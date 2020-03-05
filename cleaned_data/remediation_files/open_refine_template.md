
# Open Refine Template William Cox Cochran Collection


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="documentID">{{cells["Document_ID"].value}}</identifier>

<identifier type="pid">{{cells["PID"].value}}</identifier>

<titleInfo><title>{{cells['titleInfo_title'].value}}</title></titleInfo>

<abstract>{{cells['abstract'].value}}</abstract>

<name authority="naf" valueURI="{{cells['creator_URI'].value}}"><namePart>{{cells['creator'].value}}</namePart><role>
<roleTerm type="text" authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/pht">Photographer</roleTerm>
</role></name>

<name authority="naf" valueURI="{{cells['donor_URI'].value}}"><namePart>{{cells['donor'].value}}</namePart><role>
<roleTerm type="text" authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/dnr">Donor</roleTerm>
</role></name>

{{if(isBlank(cells['dateCreated'].value), '', '<originInfo><dateCreated>' + cells['dateCreated'].value + '</dateCreated><dateCreated encoding="edtf" keyDate="yes">' + cells['dateCreated_edtf'].value + '</dateCreated>
</originInfo>')}}

<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form></physicalDescription>







{{if(isBlank(cells['subject_4_name'].value), '', '<subject authority="naf" valueURI="' + cells['subject_4_name_URI'].value + '"><name><namePart>' + cells['subject_4_name'].value + '</namePart></name></subject>')}}


{{if(isBlank(cells['subject_6_name'].value), '', '<subject authority="naf" valueURI="' + cells['subject_6_name_URI'].value + '"><name><namePart>' + cells['subject_6_name'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_7_name'].value), '', '<subject><name><namePart>' + cells['subject_7_name'].value + '</namePart></name></subject>')}}




{{if(isBlank(cells['subject_topic'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_topic_URI'].value + '"><topic>' + cells['subject_topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_2_topic'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_2_topic_URI'].value + '"><topic>' + cells['subject_2_topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_3_topic'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_3_topic_URI'].value + '"><topic>' + cells['subject_3_topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_4_topic'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_4_topic_URI'].value + '"><topic>' + cells['subject_4_topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_5_topic'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_5_topic_URI'].value + '"><topic>' + cells['subject_5_topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_6_topic'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_6_topic_URI'].value + '"><topic>' + cells['subject_6_topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_7_topic'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_7_topic_URI'].value + '"><topic>' + cells['subject_7_topic'].value + '</topic></subject>')}}



{{if(isBlank(cells['subject_geographic_name'].value), '', '<subject' +  if(isBlank(cells['subject_geographic_URI'].value), '>', 
' authority="geonames" valueURI="' + cells['subject_geographic_URI'].value + '">') + '<geographic>' + cells['subject_geographic_name'].value + '</geographic>' + if(isBlank(cells['subject_geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}


{{if(isBlank(cells['subject_2_geographic_name'].value), '', '<subject' +  if(isBlank(cells['subject_2_geographic_URI'].value), '>', 
' authority="geonames" valueURI="' + cells['subject_2_geographic_URI'].value + '">') + '<geographic>' + cells['subject_2_geographic_name'].value + '</geographic>' + if(isBlank(cells['subject_2_geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_2_geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}


{{if(isBlank(cells['subject_3_geographic_name'].value), '', '<subject' +  if(isBlank(cells['subject_3_geographic_URI'].value), '>', 
' authority="geonames" valueURI="' + cells['subject_3_geographic_URI'].value + '">') + '<geographic>' + cells['subject_3_geographic_name'].value + '</geographic>' + if(isBlank(cells['subject_3_geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_3_geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}

{{if(isBlank(cells['subject_4_geographic_name'].value), '', '<subject' +  if(isBlank(cells['subject_4_geographic_URI'].value), '>', 
' authority="geonames" valueURI="' + cells['subject_4_geographic_URI'].value + '">') + '<geographic>' + cells['subject_4_geographic_name'].value + '</geographic>' + if(isBlank(cells['subject_4_geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_4_geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}


{{if(isBlank(cells['subject_5_geographic_name'].value), '', '<subject' +  if(isBlank(cells['subject_5_geographic_URI'].value), '>', 
' authority="geonames" valueURI="' + cells['subject_5_geographic_URI'].value + '">') + '<geographic>' + cells['subject_5_geographic_name'].value + '</geographic>' + if(isBlank(cells['subject_5_geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_5_geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}

{{if(isBlank(cells['subject_6_geographic_name'].value), '', '<subject' +  if(isBlank(cells['subject_6_geographic_URI'].value), '>', 
' authority="geonames" valueURI="' + cells['subject_6_geographic_URI'].value + '">') + '<geographic>' + cells['subject_6_geographic_name'].value + '</geographic>' + if(isBlank(cells['subject_6_geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_6_geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}

{{if(isBlank(cells['subject_7_geographic_name'].value), '', '<subject' +  if(isBlank(cells['subject_7_geographic_URI'].value), '>', 
' authority="geonames" valueURI="' + cells['subject_7_geographic_URI'].value + '">') + '<geographic>' + cells['subject_7_geographic_name'].value + '</geographic>' + if(isBlank(cells['subject_7_geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_7_geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}

{{if(isBlank(cells['subject_8_geographic_name'].value), '', '<subject' +  if(isBlank(cells['subject_8_geographic_URI'].value), '>', 
' authority="geonames" valueURI="' + cells['subject_8_geographic_URI'].value + '">') + '<geographic>' + cells['subject_8_geographic_name'].value + '</geographic>' + if(isBlank(cells['subject_8_geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_8_geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}

{{if(isBlank(cells['subject_9_geographic_name'].value), '', '<subject' +  if(isBlank(cells['subject_9_geographic_URI'].value), '>', 
' authority="geonames" valueURI="' + cells['subject_9_geographic_URI'].value + '">') + '<geographic>' + cells['subject_9_geographic_name'].value + '</geographic>' + if(isBlank(cells['subject_9_geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_9_geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}

{{if(isBlank(cells['subject_10_geographic_name'].value), '', '<subject' +  if(isBlank(cells['subject_10_geographic_URI'].value), '>', 
' authority="geonames" valueURI="' + cells['subject_10_geographic_URI'].value + '">') + '<geographic>' + cells['subject_10_geographic_name'].value + '</geographic>' + if(isBlank(cells['subject_10_geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_10_geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}


{{if(isBlank(cells['subject_11_geographic_name'].value), '', '<subject' +  if(isBlank(cells['subject_11_geographic_URI'].value), '>', 
' authority="geonames" valueURI="' + cells['subject_11_geographic_URI'].value + '">') + '<geographic>' + cells['subject_11_geographic_name'].value + '</geographic>' + if(isBlank(cells['subject_11_geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_11_geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}


{{if(isBlank(cells['subject_12_geographic_name'].value), '', '<subject' +  if(isBlank(cells['subject_12_geographic_URI'].value), '>', 
' authority="geonames" valueURI="' + cells['subject_12_geographic_URI'].value + '">') + '<geographic>' + cells['subject_12_geographic_name'].value + '</geographic>' + if(isBlank(cells['subject_12_geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_12_geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}


{{if(isBlank(cells['subject_13_geographic_name'].value), '', '<subject' +  if(isBlank(cells['subject_13_geographic_URI'].value), '>', 
' authority="geonames" valueURI="' + cells['subject_13_geographic_URI'].value + '">') + '<geographic>' + cells['subject_13_geographic_name'].value + '</geographic>' + if(isBlank(cells['subject_13_geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_13_eographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}



{{if(isBlank(cells['subject_14_geographic_name'].value), '', '<subject' +  if(isBlank(cells['subject_14_geographic_URI'].value), '>', 
' authority="geonames" valueURI="' + cells['subject_14_geographic_URI'].value + '">') + '<geographic>' + cells['subject_14_geographic_name'].value + '</geographic>' + if(isBlank(cells['subject_14_geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_14_geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}



{{if(isBlank(cells['subject_15_geographic_name'].value), '', '<subject' +  if(isBlank(cells['subject_15_geographic_URI'].value), '>', 
' authority="geonames" valueURI="' + cells['subject_15_geographic_URI'].value + '">') + '<geographic>' + cells['subject_15_geographic_name'].value + '</geographic>' + if(isBlank(cells['subject_15_geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_15_geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}

{{if(isBlank(cells['subject_16_geographic_name'].value), '', '<subject' +  if(isBlank(cells['subject_16_geographic_URI'].value), '>', 
' authority="geonames" valueURI="' + cells['subject_16_geographic_URI'].value + '">') + '<geographic>' + cells['subject_16_geographic_name'].value + '</geographic>' + if(isBlank(cells['subject_16_geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_16_geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}

{{if(isBlank(cells['subject_17_geographic_name'].value), '', '<subject' +  if(isBlank(cells['subject_17_geographic_URI'].value), '>', 
' authority="geonames" valueURI="' + cells['subject_17_geographic_URI'].value + '">') + '<geographic>' + cells['subject_17_geographic_name'].value + '</geographic>' + if(isBlank(cells['subject_17_geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_17_geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}

{{if(isBlank(cells['subject_18_geographic_name'].value), '', '<subject' +  if(isBlank(cells['subject_18_geographic_URI'].value), '>', 
' authority="geonames" valueURI="' + cells['subject_18_geographic_URI'].value + '">') + '<geographic>' + cells['subject_18_geographic_name'].value + '</geographic>' + if(isBlank(cells['subject_18_geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_18_geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}


{{if(isBlank(cells['subject_19_geographic_name'].value), '', '<subject' +  if(isBlank(cells['subject_19_geographic_URI'].value), '>', 
' authority="geonames" valueURI="' + cells['subject_19_geographic_URI'].value + '">') + '<geographic>' + cells['subject_19_geographic_name'].value + '</geographic>' + if(isBlank(cells['subject_19_geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_19_geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}

{{if(isBlank(cells['subject_20_geographic_name'].value), '', '<subject' +  if(isBlank(cells['subject_20_geographic_URI'].value), '>', 
' authority="geonames" valueURI="' + cells['subject_20_geographic_URI'].value + '">') + '<geographic>' + cells['subject_20_geographic_name'].value + '</geographic>' + if(isBlank(cells['subject_20_geographic_coordinates'].value), '', '<cartographics><coordinates>' + cells['subject_20_geographic_coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}

{{if(isBlank(cells['subject_geographic_naf'].value), '', '<subject' +  if(isBlank(cells['subject_geographic_naf_URI'].value), '>', 
' authority="naf" valueURI="' + cells['subject_geographic_naf_URI'].value + '">') + '<geographic>' + cells['subject_geographic_naf'].value + '</geographic></subject>')}}

{{if(isBlank(cells['subject_geographic_lcsh'].value), '', '<subject' +  if(isBlank(cells['subject_geographic_lcsh_URI'].value), '>', 
' authority="lcsh" valueURI="' + cells['subject_geographic_lcsh_URI'].value + '">') + '<geographic>' + cells['subject_geographic_lcsh'].value + '</geographic></subject>')}}



<typeOfResource>still image</typeOfResource>

<relatedItem displayLabel="Project" type="host"><titleInfo><title>{{cells['digital_collection'].value}}</title></titleInfo></relatedItem>

<relatedItem displayLabel="Collection" type="host">
<titleInfo>
<title>{{cells['archival_collection'].value}}</title>
</titleInfo>
<identifier>{{cells['archival_identifier'].value}}</identifier>
</relatedItem>

<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>

<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>

<accessCondition type="use and reproduction" xlink:href="{{cells['rights_URI'].value}}">{{cells['rights'].value}}</accessCondition>

</mods>

```

#### Suffix

```
</modsCollection>
```