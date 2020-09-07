# Overview
A3 Auction” is an online web portal aimed at taking the auction to the finger-tips of the aspiring bidders and sellers there by building an “On-line auction management system” which can wipe out the inherent problems of “Conventional Auction House”.
The suggested web portal will have a home page where all users can sign up and there will be display of all the latest products in the chronological order with all the auction details such as Product Name, Product Description, Starting Bid Amount, Incremental Value etc. Any user can navigate through all the products by selecting the category of the product from the drop-down menu. Only authenticated users can take part in selling or in bidding and only those who have registered and authenticated as sellers can place their products for bidding. The database also keeps the record of all the bids of an auction and the bid history related to a bidder account. There is also an administrator of the whole system who can track any auction, authenticate the users and products and can contact the seller and bidder, instructing them about the transaction details, the shipping mode etc. 

# Stakeholders Benefits
For the improvement and effective functioning of the system, buyers will also be able to give detailed seller feedback of all aspects of the seller and giving comments for example: giving comments of how accurate the item’s descriptions was, how satisfied they were with the seller’s communication and how quickly were the products transported to them by the seller.  
This database provides the customers with “Paperless Auction System” which can be accessible to everyone, at any time no matter where they are. It is designed in such a way that it is as user friendly as possible. So, any aspiring seller can visit the web site and engage in bidding with least effort. The main aim of this web portal is to make a good online system that provides a great alternative of bidding policy for general people that saves both time and money. 

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

# Business rules
1. To be a buyer or seller, a person must be 18 years of age. 
2. A buyer can participate in at most one auction at a time.  
3. Only authenticated users, approved by the admin, can take part in selling or in bidding.  
4. Only those who have registered and authenticated as sellers can place their products for bidding.  
5. Every item on sale can belong to one and only one category.  
6. Each seller or buyer can see all the items on sale.  
7. Every auction has a specified bidding time after which the winner will be declared.  
8. One product belonging to a seller can be auctioned only once.
9. Every product category must have at least one product. 

# Database Infrastructure
In this Project, the database infrastructure used is based on client-server model. SQL server is used as the database engine and Access is used as the interface design tool. Data are controlled and managed using SQL server database i.e. insertion, deletion and updating of data is done using SQL queries and interface is generated using Access forms and reports. All the data stored in SQL database can also be viewed using Access as reports and data can be manipulated (insertion, deletion) using Access forms.   
