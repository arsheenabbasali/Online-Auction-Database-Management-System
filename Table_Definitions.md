## [Overview](README.md)

## [Entity Relationship Diagram](Entity_Database/Entity_Relationship.md)

# Tables Definition

## [Major Data Questions](Data_Questions.md)

## [Interface](Interface/Interface_forms.md) 

### SQL Scripts for Table Creation

 **Administrator Table**: 
 ```sql
create table Administrator ( 
Admin_ID INTEGER NOT NULL PRIMARY KEY, 
Admin_FName varchar(20) Not null, 
Admin_LName varchar(20) not null, 
Admin_StreetNo integer not null, 
Admin_StreetName varchar(100) not null, 
Admin_City varchar(50) not null, 
Admin_State varchar(20) not null, 
Amin_zipcode integer not null, 
Admin_Country varchar(40) not null, 
Admin_Email varchar(40) not null, 
Admin_PhoneNo integer not null  
); 
```
**Users Table**: 
```sql
create table Users( 
User_ID integer not null primary key,   
User_FName varchar(20) not null, 
User_LName varchar(20) not null, 
User_StreetNo integer not null, 
User_StreetName varchar(100) not null,
User_City varchar(50) not null, 
User_State integer not null, 
User_Zipcode integer not null, 
User_Country varchar(40) not null, 
User_Email varchar(40) not null, 
User_PhoneNo integer not null, 
User_Admin_ID integer not null foreign key references Admin(Admin_ID) 
);  
```
**Product_Category Table**: 
```sql
create table Product_Category( 
Prod_Cat_ID integer not null primary key, 
Prod_Cat_Name varchar(30) not null
);
```
**Product Table**: 
```sql
create table Product( 
Prod_ID integer not null primary key, 
Prod_Name varchar(40) not null, 
Prod_Description varchar(400) not null, 
Prod_Start_Bid_Amount money not null, 
Min_Bid_Increment money, 
Seller_ID integer not null foreign key references Users(User_ID), 
Prod_Cat_ID integer not null foreign key references Product_Category(Prod_Cat_ID)
); 
```
**Auction Table**: 
```sql
create table Auction( 
Auc_ID integer not null primary key, 
Auc_Start_Date date not null, 
Auc_Close_Date date not null, 
Auc_Reserve_Price money not null, 
Auc_Payment_Date date, 
Auc_Winner_FName varchar(20) not null, 
Auc_Winner_LName varchar(20) not null, 
Auc_Payment_Amount money, 
Auc_Item_ID integer not null foreign key references Product(Prod_ID)
); 
```
**Feedback Table**: 
```sql
create table Feedback( 
Fdb_ID integer not null primary key, 
Fdb_Time time not null, 
Fdb_Date date not null, 
Satisfaction_rating integer not null, 
Shipping_Delivery integer not null,  
Seller_Cooperation integer not null,  
Overall_Rating integer not null, 
Seller_ID integer not null foreign key references Users(User_ID), 
Buyer_ID integer not null foreign key references Users(User_ID)
); 
``` 
**Bid Table**: 
```sql
create table Bid( 
Bid_Number integer not null, 
Bid_Item_ID integer not null foreign key references Product(Prod_ID), 
Bid_Time time not null,
Bid_Date date not null, 
Bid_Price money not null, 
Bid_Comment varchar(200), 
Bidder_ID integer not null foreign key references Users(User_ID), 
Seller_ID integer not null foreign key references Users(User_ID), 
Auc_ID integer not null foreign key references Auction(Auc_ID) primary key(Bid_Number, Bid_Item_ID) 
); 
``` 
**Shipment Table**: 
```sql
create table Shipment( 
Shipment_ID integer not null primary key, 
Ship_Planned_Date date not null, 
Ship_Actual_Date date not null,  
Ship_Cost money, 
Ship_Item_ID integer not null foreign key references Product(Prod_ID) 
); 
``` 
**Payment_Method Table**: 
```sql
create table Payment_Method( 
Pay_Method_Code integer not null primary key,
Pay_Method_Description varchar(200) not null, 
Auc_ID integer not null foreign key references Auction(Auc_ID)
); 
```
