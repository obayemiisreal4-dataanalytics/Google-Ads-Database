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
Advertiser - Campaign: One advertiser can manage multiple campaigns, but each campaign belongs to a single advertiser (one-to-many) <br>.
Campaign – Ad: One campaign can contain multiple ads, but each ad is linked to one campaign (one-to-many) <br>.
Ad - Keyword: An ad can target multiple keywords, but each keyword is associated with one ad (one-to-many) <br>.
Ad - Performance: One ad can generate multiple performance records over time, but each performance record belongs to a specific ad (one-to-many) <br>. 

## Entity Relationship Diagram 
The Entity Relationship Diagram shows the collection of objects within a database and the relationship between them. It includes the entities, Schemas, Participation constraints and the relationship between the entities, I modeled this using the ERD tools by defining the table and specifying the relationships between the tabbles using pre-existing columns as foreign keys.

![Google Database Entity Relationship Diagram]![Uploading ERD GOOGLE DB PICTURE.png…](ERD.png)

## Advertiser table

'''Sql
INSERT INTO Advertiser (AdvertiserID, Advertisername, Contactperson, Contactemail, Phonenumber)
VALUES
(1, 'Simtech Creative', 'Chinwe Okoro', 'chimweokoro@gmail.com', '+234 (0)70 4735 0000'),
(2, 'Gain Infinity - Digital Marketing Agency', 'Emeka Ibe', 'emekaibe@gmail.com', '+234 (0)70 6183 9068'),
(3, 'Businete Digital Agency', 'Kehinde Adebayo', 'kehindeadebayo@yahoo.com', '+234 (0)90 2726 9753'),
(4, 'Algorithm Media', 'Funke Adewale', 'funkeadewale@gmail.com', '+234 (0)70 4735 0001'),
(5, 'Super Stars Promotions Limited', 'Ifeanyi Inwachukwu', 'ifeanyiinwachukwu@yahoo.com', '+234 (0)70 6183 9069'),
(6, 'Stanoz Designs', 'Ngozi Obi', 'ngoziobi@gmail.com', '+234 (0)90 2726 9754'),
(7, 'Alternative Adverts Ltd', 'Tolu Onifade', 'toluonifade@yahoo.com', '+234 (0)70 4735 0002'),
(8, 'Betteroffservice, Advertising Agency', 'Bayo Alabi', 'bayoalabi@gmail.com', '+234 (0)70 6183 9070'),
(9, 'Odichi Solutions', 'Zainab Abdullahi', 'zainababdullahi@yahoo.com', '+234 (0)90 2726 9755'),
(10, 'Gems Communications Ltd', 'Yakubu Danladi', 'yakubudanladi@gmail.com', '+234 (0)70 4735 0003'),
(11, 'Wetherheads, Advertising Group', 'Amara Umeh', 'amaraumeh@gmail.com', '+234 (0)70 6183 9071'),
(12, 'Adhubbing', 'Abdullahi Musa', 'abdullahimusa@yahoo.com', '+234 (0)90 2726 9756'),
(13, 'Ellae Creative', 'Esther Ogunleye', 'estherogunleye@gmail.com', '+234 (0)70 4735 0004');

describe advertiser;
select * from advertiser;







