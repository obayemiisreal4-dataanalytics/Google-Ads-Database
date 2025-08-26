# Google-Ads-Database
Google is a multinational technology company offering online advertising services through the Google Ads platform. As a data analyst, you have been tasked with developing a comprehensive Relational Database Management System (RDBMS) to support Google Ads operations. The goal is to manage advertisers,campaigns,ads, keywords, and performance metrics.

## Objectives
* Identifying the main entities in the database system.
* Clearly defining the attributes, relationships and constraint that support the business needs.
* Designing an entity relationship diagram that supports the business needs based on the database entities, relatinships and participation constraints.


  
## Main Entities in the table
Entities are tables or real world objects that are meant to store information in the database. They are fundamental component of an Entity Relationship Diagram(ERD).

# Advertiser
This is the table that stores the advertisers' information. The attributes and data types are as follows:<br>
AdvertiserID **INT**<br>
AdvertiserName **VARCHAR**<br>
ContactPerson **VARCHAR**<br>
ContactEmail **VARCHAR**<br>

## Campaign
This is the table that stores information from the campaigns. The attributes and data types are as follows:<br>
CampaignID **INT**<br>
AdvertiserID **INT**<br>
CampaignName **VARCHAR**<br>
StartDate **DATE**<br>

## Advertisement
This is the table that stores information from the advertisement. The attributes and data types are as follows:<br>
AdID **INT**<br>
CampaignID **INT**<br>
AdTitle **VARCHAR**<br>
TargetURL **VARCHAR**<br>
Impression **SMALLINT**<br>

## keyword
This is the table that stores information from the keyword. The attributes and data types are as follows:<br>
keywordid **INT**<br>
adid **INT** <br>
keywordtext **TEXT** <br>
Bidamount **SNALLINT** <br>
QualityScore **SMALLINT** <br>

## Performance
This is the table that stores information from the Performance. The attributes and data types are as follows:<br>
Performanceid **INT** <br>
Adid **INT** <br>
Date **DATE** <br>
Clicks **SMALLINT** <br>
Conversations **SMALLINT** <br>


