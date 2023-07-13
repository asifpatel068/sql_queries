Set 3 problems:

**Problem 26:**
- **Prerequisite**: Understand creating tables in SQL / collections in MongoDB
- **Problem**: Create a **`Rides`** table / collection with the fields defined above.

**Solution 26:**
To create the `Rides` table, we'll use the following SQL query:
```sql
CREATE TABLE Rides (
    id INT PRIMARY KEY,
    driver_id INT,
    passenger_id INT,
    start_location VARCHAR(255),
    end_location VARCHAR(255),
    distance DECIMAL(5,2),
    ride_time DECIMAL(5,2),
    fare DECIMAL(6,2)
);
```
Explanation: This query creates a table named `Rides` with the specified fields: `id`, `driver_id`, `passenger_id`, `start_location`, `end_location`, `distance`, `ride_time`, and `fare`. The `id` field is set as the primary key to uniquely identify each ride.

**Problem 27:**
- **Prerequisite**: Understand inserting data into SQL tables / MongoDB collections
- **Problem**: Insert five rows / documents into the **`Rides`** table / collection with data of your choice.

**Solution 27:**
To insert data into the `Rides` table, we'll use the following SQL query:
```sql
INSERT INTO Rides (id, driver_id, passenger_id, start_location, end_location, distance, ride_time, fare)
VALUES
    (1, 101, 201, 'A', 'B', 5.2, 15, 10.5),
    (2, 102, 202, 'C', 'D', 3.8, 10, 8.2),
    (3, 103, 203, 'E', 'F', 7.5, 20, 15.0),
    (4, 104, 204, 'G', 'H', 2.3, 8, 6.5),
    (5, 105, 205, 'I', 'J', 4.6, 12, 9.8);
```
Explanation: This query inserts five rows into the `Rides` table, each representing a ride with different values for the fields. You can customize the values according to your preference.



Certainly! Here are the solutions to the next set of problems:

**Problem 28:**
- **Prerequisite**: Understand how to order data in SQL / MongoDB
- **Problem**: Write a query to fetch all rides, ordered by **`fare`** in descending order.

**Solution 28:**
```sql
SELECT * FROM Rides ORDER BY fare DESC;
```
Explanation: This query selects all columns (`*`) from the `Rides` table and orders the result in descending order based on the `fare` column. This will fetch all rides from the table, sorted by their fare in descending order.

**Problem 29:**
- **Prerequisite**: Understand using math operations in SQL / MongoDB
- **Problem**: Write a query to calculate the total **`distance`** and total **`fare`** for all rides.

**Solution 29:**
```sql
SELECT SUM(distance) AS total_distance, SUM(fare) AS total_fare FROM Rides;
```
Explanation: This query uses the `SUM` function to calculate the sum of the `distance` and `fare` columns in the `Rides` table. It returns the total distance as `total_distance` and the total fare as `total_fare`.

**Problem 30:**
- **Prerequisite**: Understand how to use the AVG function in SQL / MongoDB's aggregate functions
- **Problem**: Write a query to calculate the average **`ride_time`** of all rides.

**Solution 30:**
```sql
SELECT AVG(ride_time) AS average_ride_time FROM Rides;
```
Explanation: This query uses the `AVG` function to calculate the average of the `ride_time` column in the `Rides` table. The result is returned as `average_ride_time`.

**Problem 31:**
- **Prerequisite**: Understand using string patterns in SQL (LIKE clause) / using regex in MongoDB
- **Problem**: Write a query to fetch all rides whose **`start_location`** or **`end_location`** contains 'Downtown'.

**Solution 31:**
```sql
SELECT * FROM Rides WHERE start_location LIKE '%Downtown%' OR end_location LIKE '%Downtown%';
```
Explanation: This query selects all columns (`*`) from the `Rides` table where either the `start_location` or `end_location` contains the string 'Downtown'. The `%` symbol is a wildcard that matches any number of characters, so it will fetch all rides whose start or end location includes the phrase 'Downtown'.

**Problem 32:**
- **Prerequisite**: Understand how to use the COUNT function in SQL / MongoDB's aggregate functions
- **Problem**: Write a query to count the number of rides for a given **`driver_id`**.

**Solution 32:**
```sql
SELECT COUNT(*) AS ride_count FROM Rides WHERE driver_id = <driver_id>;
```
Explanation: This query uses the `COUNT` function to count the number of rows in the `Rides` table where the `driver_id` matches the specified value. Replace `<driver_id>` with the actual driver ID you want to count the rides for. The result is returned as `ride_count`.

**Problem 33:**
- **Prerequisite**: Understand data updating in SQL / MongoDB
- **Problem**: Write a query to update the **`fare`** of the ride with **`id`** 4.

**Solution 33:**
```sql
UPDATE Rides SET fare = <new_fare> WHERE id = 4;
```
Explanation: This query uses the `UPDATE` statement to update the `fare` column in the `Rides` table. Replace `<new_fare>` with the new fare value you want to set for the ride with ID 4.

**Problem 34:**
- **Prerequisite**: Understand using GROUP BY in SQL / MongoDB's aggregate functions
- **Problem**: Write a query to calculate the total **`fare`** for each **`driver_id`**.

**Solution 34:**
```sql
SELECT driver_id, SUM(fare) AS total_fare FROM Rides GROUP BY driver_id;
```
Explanation: This query uses the `SUM` function and `GROUP BY` clause to calculate the total fare for each driver ID in the `Rides` table. It returns the driver ID and the corresponding total fare as `total_fare`.

**Problem 35:**
- **Prerequisite**: Understand data deletion in SQL / MongoDB
- **Problem**: Write a query to delete the ride with **`id`** 2.

**Solution 35:**
```sql
DELETE FROM Rides WHERE id = 2;
```
Explanation: This query uses the `DELETE` statement to remove the row from the `Rides` table where the `id` is 2. It will delete the ride with the specified `id`.



