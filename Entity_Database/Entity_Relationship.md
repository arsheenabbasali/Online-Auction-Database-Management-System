# Database Infrastructure
In this Project, the database infrastructure used is based on client-server model. SQL server is used as the database engine and Access is used as the interface design tool. Data are controlled and managed using SQL server database i.e. insertion, deletion and updating of data is done using SQL queries and interface is generated using Access forms and reports. All the data stored in SQL database can also be viewed using Access as reports and data can be manipulated (insertion, deletion) using Access forms.   

# Entities
1. **User**: This entity captures information about the buyer or seller who signed up on the online auction web portal. 
2. **Administrator**: The entity captures the information about all the individuals who are responsible for the functioning of web portal.
3. **Product**: This entity captures the information about all the products which are available for the auction. 
4. **Auction**: This entity captures the information about any product which is already being auctioned. 
5. **Feedback**: This entity captures the information about reaction/feedback of any buyer or seller about any product auction.
6. **Bid**: This entity captures the information about the bid any buyer has put for a product i.e. the price a buyer is willing to pay in an auction.
7. **Product_Category**: The entity captures the information about the category in which a specific product belongs. 
8. **Shipment**: The entity captures the information about the shipment details of a sold product after an auction.
9. **Payment_Method**: This entity captures the information about chosen payment method for any sold product by a buyer or accepted payment methods by seller for any product.  

# Entity Relationship Diagram
![png](Entity_Database/Entity%20Diagram.jpg)
