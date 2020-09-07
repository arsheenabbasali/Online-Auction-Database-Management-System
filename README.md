# Overview

## [Entity Relationship Diagram](Entity_Database/Entity_Relationship.md)

## [Tables Definition](Table_Definitions.md)

### Introduction
A3 Auction” is an online web portal aimed at taking the auction to the finger-tips of the aspiring bidders and sellers there by building an “On-line auction management system” which can wipe out the inherent problems of “Conventional Auction House”.
The suggested web portal will have a home page where all users can sign up and there will be display of all the latest products in the chronological order with all the auction details such as Product Name, Product Description, Starting Bid Amount, Incremental Value etc. Any user can navigate through all the products by selecting the category of the product from the drop-down menu. Only authenticated users can take part in selling or in bidding and only those who have registered and authenticated as sellers can place their products for bidding. The database also keeps the record of all the bids of an auction and the bid history related to a bidder account. There is also an administrator of the whole system who can track any auction, authenticate the users and products and can contact the seller and bidder, instructing them about the transaction details, the shipping mode etc.

### Problem Statement
The current auction system involves people attending auction sessions which were set at a definite time. Some would not make it because were travelling from far places and so most of the time they would miss the sessions. Moreover, this causes the waste of time and money to travel from far off places to buy one item.
Moreover, the auction houses are not for every individual, they are for the selected few with tickets to attend. This limits the people with no authorization although those people may have an interest in buying some products.
This auction also covers a small geographical area, for example a person in California may not be aware of an auction taking place in Miami. This makes the auctions to be attended by small amount of people and may be unable for the seller to get the expected price of the product.

### Stakeholders Benefits
For the improvement and effective functioning of the system, buyers will also be able to give detailed seller feedback of all aspects of the seller and giving comments for example: giving comments of how accurate the item’s descriptions was, how satisfied they were with the seller’s communication and how quickly were the products transported to them by the seller.  
This database provides the customers with “Paperless Auction System” which can be accessible to everyone, at any time no matter where they are. This online-auction provides the customers with great advantages of low prices, greater product selection and greater efficiency compared to the usual traditional offline markets. It is designed in such a way that it is as user friendly as possible. So, any aspiring seller can visit the web site and engage in bidding with least effort. The main aim of this web portal is to make a good online system that provides a great alternative of bidding policy for general people that saves both time and money.

### Business rules
1. To be a buyer or seller, a person must be 18 years of age. 
2. A buyer can participate in at most one auction at a time.  
3. Only authenticated users, approved by the admin, can take part in selling or in bidding.  
4. Only those who have registered and authenticated as sellers can place their products for bidding.  
5. Every item on sale can belong to one and only one category.  
6. Each seller or buyer can see all the items on sale.  
7. Every auction has a specified bidding time after which the winner will be declared.  
8. One product belonging to a seller can be auctioned only once.
9. Every product category must have at least one product. 


