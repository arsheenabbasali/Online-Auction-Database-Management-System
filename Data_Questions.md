## [Overview](README.md)

## [Entity Relationship Diagram](Entity_Database/Entity_Relationship.md)

## [Tables Definition](Table_Definitions.md)

# Major Data Questions

## [Interface](Interface/Interface_forms.md)

## [Reports](Reports/Reports.md)

### Answering Major Data Questions

1. **Details of an Auction of a Product.** 
```sql
select distinct U.User_FName + ' ' + U.User_LName as [Seller Name] , P.Prod_Name, P.Prod_Description, A.Auc_Reserve_Price as [Starting Bid Price], A.Auc_Payment_Amount as [Selling Price], A.Auc_Winner_FName + ' ' + A.Auc_Winner_LName as [Buyer Name], S.Ship_Planned_Date, S.Ship_Actual_Date, S.Ship_Cost 
from Users as U Join Product as P on U.User_ID = P.Seller_ID 
Join Bid as B on B.Bid_Item_ID = P.Prod_ID Join Shipment as S on S.Ship_Item_ID = P.Prod_ID 
Join Auction as A on A.Auc_ID = B.Auc_ID 
where P.Prod_Name = 'Baseball';
```

2. **Sellers who have highest rating (Popular Seller).** 
```sql
select Seller_ID, avg(Overall_Rating) as rating into #TempTable 
from Feedback group by Seller_ID; 
 
select User_FName + ' ' + User_LName as Name, User_State, User_Country, TT.rating 
from Users as U Join #TempTable as TT on U.User_ID = TT.Seller_ID 
where U.User_ID in (select Seller_ID from #TempTable where rating = (select max(rating) from #TempTable));
```
 
3. **List all the bids placed for a particular product.**
 ```sql
select Bid_Time, Bid_Date, Bid_Price, U.User_FName, U.User_LName 
from Bid as B join Users as U on B.Bidder_ID= U.User_ID join Product as P on P.Prod_ID = B.Bid_Item_ID 
where P.Prod_Name= 'Baseball'; 
```
 
4. **Which Product got highest number of bids?**
```sql
select Prod_Cat_Name, P.Prod_Name 
from Product_Category as PC Join Product as P on PC.Prod_Cat_ID = P.Prod_Cat_ID 
where P.Prod_ID = (select Bid_Item_ID from  (SELECT Bid_Item_ID , COUNT(*) AS num FROM Bid GROUP BY Bid_Item_ID)a 
where num = (select max(num) from (SELECT Bid_Item_ID , COUNT(*) AS num FROM Bid GROUP BY Bid_Item_ID) a)); 
```

5. **Name all the products bought by a Buyer.** 
```sql
select distinct Prod_Name, Prod_Description, A.Auc_Payment_Amount as Final_Price 
from Product as P Join Bid as B on P.Prod_ID = B.Bid_Item_ID  
Join Auction as A on A.Auc_ID = B.Auc_ID 
where A.Auc_Winner_FName = 'Alvina' and A.Auc_Winner_LName='Kulicke'; 
```

6. **State all the information about the Buyer of a product.** 
```sql
select User_FName + ' ' + User_LName as FullName, User_StreetNo, User_StreetName, User_City, User_State, User_Zipcode  as User_Address, User_Country, User_Email, User_PhoneNo
from Users  as U Join Product as P on U.User_ID = P.Seller_ID 
where P.Prod_Name = 'Dishwasher'; 
```
 
 
 
