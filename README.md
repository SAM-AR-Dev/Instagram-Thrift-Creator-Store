# Instagram-Thrift-Creator-Store

https://app.eraser.io/workspace/RR2JpRGP0NGJkceKLsht?origin=share

Here is a README file you can use for your project. It explains the process clearly and keeps things concise.

***

# Instagram Thrift & Handmade Store ER Diagram

This README explains how I designed the Entity-Relationship (ER) diagram for an Instagram-based thrift and handmade store using diagram-as-code.

## Tool Used
I used **Eraser.io**. It is a tool that allows you to generate visual database models simply by typing structured code. 

## How I Made It

### 1. Defining the Entities (Tables)
First, I created the main tables required to run the store. In Eraser, you define an entity using its name followed by curly braces `{}`. Inside the braces, I listed the columns along with their data types (like `int`, `varchar`, `boolean`). I also added icons and colors to the table headers for better visual organization.

### 2. Setting Primary and Foreign Keys
To keep the data organized and connected, I assigned keys to specific columns.
* **pk (Primary Key):** I added this to unique identifiers like `user_id` and `product_id` to ensure every record is distinct.
* **fk (Foreign Key):** I added this to columns that need to link to other tables, such as putting a `user_id` inside the `orders` table.

### 3. Handling Different Product Types
Because the store sells both one-of-a-kind items and items made in batches, I created specific tables for `thrift_items` and `handmade_items`. Both of these link back to a central `products` table. I also added a `stocks` table to track how many items are available and an `attribute` table to manage sizes and types.

### 4. Creating Relationships
At the bottom of the code block, I defined how all these tables connect to each other using relational symbols.
* The `>` and `<` symbols create relationship lines between the tables.
* For example, typing `users.user_id > payments.user_id` draws a line connecting a customer to their payment record.
* I linked the `shipping_address` details directly to the `shipping` tracking table to ensure orders go to the right place.

## Core Database Structure
* **User Management:** `users`, `shipping_address`, `wishlist`
* **Inventory:** `products`, `thrift_items`, `handmade_items`, `stocks`, `attribute`
* **Transactions:** `orders`, `payments`, `shipping`

By writing this structured code, the Eraser platform automatically generated the clean visual diagram showing all tables and their exact connections.
