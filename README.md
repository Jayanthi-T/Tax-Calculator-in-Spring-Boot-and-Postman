# Tax Calculator

# Billing System : The Tax Problem 

Calculate and apply basic sales tax for the products sold in a departmental store.

## Description

A department store needs to calculate and apply basic sales tax for the products sold in its stores. Sales tax is applied as standard 10% for all items, except Books, Food and Medical products.

An additional 5% import duty is levied on all imported products, with no exceptions.

Write a program to prepare and print the receipt for every purchase. The receipt should list the name of all the items and their price (including tax), finishing with the total cost of the items, and the total amounts of sales taxes paid. 
The rounding rulesfor sales tax are that for a tax rate of n%, a shelf price of p contains (np/100 rounded up to the nearest 0.05) amount of sales tax.

## Getting Started

### Dependencies

* Java 15.0.3
* MySQL 8.0.27
* Spring Web
* Spring Data JPA
* MySQL Driver
* Spring Boot Devtools

### Running the Project

* Change the sql username and password in "application.properties" according to your mysql installation
* Run the BillingSystemApplication.java class as spring boot application

### Endpoints 
#### GET
```
GET  /products
```
This GET endpoint displays all the products available in the database in JSON format.

```
POST  /products/new
```
For POST request, give the input in JSON format that includes Product Type,Quantity and Unit Price. 

```
{
    "productType" : "book",
    "quantity" : 5,
    "unitPrice" : 21.33
}
```

This POST endpoint displays the tax and price of each product that is newly added.

```
DELETE  /products/{id}
```
This DELETE endpoint deletes the product with the particular id and returns the message "Deleted the Product successfully!".
If a product with the specified id doesn't exits, then returns a message like "No such Product to delete from your bill!".

```
/TotalPrice
```
This GET request displays the Total Price of the products bought.

```
/TotalTax
```
This GET request displays the Total Tax of the products bought.



## Author

Jayanthi-T


## License

This project is licensed under the [Jayanthi-T] License 
