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
AdvertiserID PK **INT**<br>
AdvertiserName **VARCHAR**<br>
ContactPerson **VARCHAR**<br>
ContactEmail **VARCHAR**<br>

## Campaign
This is the table that stores information from the campaigns. The attributes and data types are as follows:<br>
CampaignID PK **INT**<br>
AdvertiserID FK **INT**<br>
CampaignName **VARCHAR**<br>
StartDate **DATE**<br>

## Advertisement
This is the table that stores information from the advertisement. The attributes and data types are as follows:<br>
AdID PK **INT**<br>
CampaignID FK **INT**<br>
AdTitle **VARCHAR**<br>
TargetURL **VARCHAR**<br>
Impression **SMALLINT**<br>

## keyword
This is the table that stores information from the keyword. The attributes and data types are as follows:<br>
keywordid PK **INT**<br>
adid **INT** FK <br>
keywordtext **TEXT** <br>
Bidamount **SNALLINT** <br>
QualityScore **SMALLINT** <br>

## Performance
This is the table that stores information from the Performance. The attributes and data types are as follows:<br>
Performanceid PK **INT** <br>
Adid FK **INT** <br>
Date **DATE** <br>
Clicks **SMALLINT** <br>
Conversations **SMALLINT** <br>

## The cardinality requirement for the Database
Advertiser - Campaign: One advertiser can manage multiple campaigns, but each campaign belongs to a single advertiser (one-to-many).
Campaign – Ad: One campaign can contain multiple ads, but each ad is linked to one campaign (one-to-many).
Ad - Keyword: An ad can target multiple keywords, but each keyword is associated with one ad (one-to-many).
Ad - Performance: One ad can generate multiple performance records over time, but each performance record belongs to a specific ad (one-to-many). 

## Entity Relationship Diagram 
The Entity Relationship Diagram shows the collection of objects within a database and the relationship between them. It includes the entities, Schemas, Participation constraints and the relationship between the entities, I modeled this using the ERD tools by defining the table and specifying the relationships between the tabbles using pre-existing columns as foreign keys.




