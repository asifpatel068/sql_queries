# sql_queries_set1

markdown
Copy code
# MySQL Problem Statements and Solutions

## Problem 1:
- **Prerequisite**: Understand creating tables in SQL / collections in MongoDB
- **Problem**: Create a **`Customers`** table / collection with the following fields: **`id`** (unique identifier), **`name`**, **`email`**, **`address`**, and **`phone_number`**.

## Solution 1:
```sql
CREATE TABLE Customers (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100),
    address VARCHAR(255),
    phone_number VARCHAR(50)
);
```
## Problem 2:
Prerequisite: Understand inserting data into SQL tables / MongoDB collections
Problem: Insert five rows / documents into the Customers table / collection with data of your choice.
## Solution 2:
sql
Copy code
INSERT INTO Customers (id, name, email, address, phone_number)
VALUES
    (1, 'John Doe', 'john@example.com', '123 Main St', '123-456-7890'),
    (2, 'Jane Smith', 'jane@example.com', '456 Elm St', '987-654-3210'),
    (3, 'David Johnson', 'david@example.com', '789 Oak Ave', '555-123-4567'),
    (4, 'Sarah Williams', 'sarah@example.com', '321 Pine Rd', '111-222-3333'),
    (5, 'Michael Brown', 'michael@example.com', '567 Maple Ln', '444-555-6666');
Problem 3:
Prerequisite: Understand basic data fetching in SQL / MongoDB
Problem: Write a query to fetch all data from the Customers table / collection.
Solution 3:
sql
Copy code
SELECT * FROM Customers;
Problem 4:
Prerequisite: Understand how to select specific fields in SQL / MongoDB
Problem: Write a query to select only the name and email fields for all customers.
Solution 4:
sql
Copy code
SELECT name, email FROM Customers;
Problem 5:
Prerequisite: Understand basic WHERE clause in SQL / MongoDB's find method
Problem: Write a query to fetch the customer with the id of 3.
Solution 5:
sql
Copy code
SELECT * FROM Customers WHERE id = 3;
Problem 6:
Prerequisite: Understand how to use string patterns in SQL (LIKE clause) / using regex in MongoDB
Problem: Write a query to fetch all customers whose name starts with 'A'.
Solution 6:
sql
Copy code
SELECT * FROM Customers WHERE name LIKE 'A%';
Problem 7:
Prerequisite: Understand how to order data in SQL / MongoDB
Problem: Write a query to fetch all customers, ordered by name in descending order.
Solution 7:
sql
Copy code
SELECT * FROM Customers ORDER BY name DESC;
Problem 8:
Prerequisite: Understand data updating in SQL / MongoDB
Problem: Write a query to update the address of the customer with id 4.
Solution 8:
sql
Copy code
UPDATE Customers SET address = 'New Address' WHERE id = 4;
Problem 9:
Prerequisite: Understand how to limit results in SQL / MongoDB
Problem: Write a query to fetch the top 3 customers when ordered by id in ascending order.
Solution 9:
sql
Copy code
SELECT * FROM Customers ORDER BY id ASC LIMIT 3;
Problem 10:
Prerequisite: Understand data deletion in SQL / MongoDB
Problem: Write a query to delete the customer with id 2.
Solution 10:
sql
Copy code
DELETE FROM Customers WHERE id = 2;
Problem 11:
Prerequisite: Understand how to count rows / documents in SQL / MongoDB
Problem: Write a query to count the number of customers.
Solution 11:
sql
Copy code
SELECT COUNT(*) AS customer_count FROM Customers;
Problem 12:
Prerequisite: Understand how to skip rows / documents in SQL / MongoDB
Problem: Write a query to fetch all customers except the first two when ordered by id in ascending order.
Solution 12:
sql
Copy code
SELECT * FROM Customers ORDER BY id ASC LIMIT 2, 18446744073709551615;
Problem 13:
Prerequisite: Understand how to use OR conditions in SQL / MongoDB
Problem: Write a query to fetch all customers whose id is less than 3 or name ends with 's'.
Solution 13:
sql
Copy code
SELECT * FROM Customers WHERE id < 3 OR name LIKE '%s';
Problem 14:
Prerequisite: Understand how to use NULL checks in SQL / MongoDB
Problem: Write a query to fetch all customers where the phone_number field is not set or is null.
Solution 14:
sql
Copy code
SELECT * FROM Customers WHERE phone_number IS NULL OR phone_number = '';

