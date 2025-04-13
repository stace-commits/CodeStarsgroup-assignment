#  Bookstore Database Schema

This repository contains the schema design for a *Bookstore Management System*. The database supports the operations of a typical bookstore, including managing customers, books, authors, orders, shipping, and inventory tracking.

## Schema Overview

The database consists of the following key entities:

- *Customer Management*
  - customer – Stores customer profiles.
  - customer_address – Links customers to multiple addresses.
  - address – Stores address details.
  - address_status – Tracks the status of each address,(Active and Inactive).
  - 

- *Book Management*
  - book – Core book information .
  - book_author – Many-to-many mapping between books and authors.
  - author – Stores author profiles.
  - book_language – Stores supported languages for books.
  - publisher – Publisher information for each book.

- *Order & Shipping*
  - cust_order – Customer orders; references order status and shipping.
  - order_line – Line items in each order (book, quantity, price).
  - order_history – Tracks status changes of orders over time.
  - order_status – Describes each order's status (e.g., Pending, Shipped).
  - shipping_method – Available shipping options.

- *Location*
  - country – Stores country data for use in addresses and shipping.

## Entity Relationship Highlights

- A customer can have multiple addresses.
- A book can have multiple authors, and an author can write multiple books.
- Each order has one or more order lines.
- cust_order.status_id links to order_status for tracking.
- order_history provides a timeline of status changes per order.
- All addresses and customers are linked through foreign keys for normalization and consistency.

##  Technologies

- Relational Database:  MySQL.
- We used draw.io to visualize the schema.Find the ERD in our repository.

