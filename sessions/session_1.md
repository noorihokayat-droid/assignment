## <center><h1> session - 1 : Database Introduction & SQL Bas</h1></center>



 ## TASK-1 : CREATE A NEW DATABASE NAMED 'music_streaming_app'
    
    create DATABASE music_streaming_app;


## TASK-2 : INSIDE THE 'music_streaming_app' DATABASE , CREATE A TABLE CALLED  'PLAYLISTS' WITH COLUMNS : PLAYLIST_ID(INTEGER,PRIMARY KEY),NAME(VARCHAR),AND CREATED_BY(VARCHAR) 

    create table playlists (
    playlist_id int AUTO_INCREMENT PRIMARY KEY,
    name varchar(255),
    created_by varchar(255)
    );


## TASK-3 : Insert three sample rows into the 'playlists' table representing playlists like 'Bollywood Hits', 'Chill Vibes', and 'Workout Mix', each created by a different user.

    insert into playlists (name ,created_by)values('bollywood Hits','Amit'),('chill vibes','riya'),('workout mix','suresh');


## TASK-4: Write an SQL SELECT query to display all playlists created by the user 'Amit' from the 'playlists' table.<br><br><em><strong>Hint:</strong> Use the WHERE clause to filter by the 'created_by' column.</em>

    select * from playlists where created_by='amit';

![alt text](<Screenshot 2026-08-05 175331-1.png>)

## TASK-5:explain the difference between a table, a row, and a column in SQL using an example from a food delivery app like Zomato.

    
## Example Using a Food Delivery Application (Zomato)

## Introduction

In SQL, data is organized in the form of **tables**, which consist of **rows** and **columns**. Understanding the difference between these three components is essential for designing and managing databases effectively. The following example uses a food delivery application like **Zomato** to explain each concept.

---

# 1. Table

A **Table** is a collection of related data organized into rows and columns. Each table stores information about a specific entity, such as restaurants, customers, or orders.

### Example: `Restaurants` Table

| RestaurantID | RestaurantName | City       | Cuisine  | Rating |
|--------------|----------------|------------|-----------|--------|
| 101 | Pizza Hub | Surat | Italian | 4.5 |
| 102 | Burger Point | Rajkot | Fast Food | 4.2 |
| 103 | Spice Villa | Ahmedabad | Indian | 4.7 |

**Explanation:**
- The **Restaurants** table stores information about restaurants available on Zomato.
- Each row represents one restaurant.
- Each column represents a specific attribute of the restaurant.

---

# 2. Row

A **Row** (also called a **Record** or **Tuple**) represents a single entry in a table. It contains complete information about one entity.

### Example of One Row

| RestaurantID | RestaurantName | City | Cuisine | Rating |
|--------------|----------------|------|----------|--------|
| 101 | Pizza Hub | Surat | Italian | 4.5 |

**Explanation:**
This row contains all the details of **Pizza Hub**, including its unique ID, city, cuisine type, and customer rating.

---

# 3. Column

A **Column** (also called a **Field** or **Attribute**) represents a specific category of information stored in the table. Every column contains values of the same type for all records.

### Example Columns

| Column Name | Description |
|-------------|-------------|
| RestaurantID | Unique identification number of the restaurant |
| RestaurantName | Name of the restaurant |
| City | City where the restaurant is located |
| Cuisine | Type of food served |
| Rating | Customer rating of the restaurant |

---

# Difference Between Table, Row, and Column

| Feature | Table | Row | Column |
|---------|-------|-----|--------|
| Definition | Collection of related data | A single record in a table | A specific attribute of the data |
| Stores | Multiple records | One complete record | One type of information |
| Example | Restaurants table | Pizza Hub details | RestaurantName, City, Rating |
| Also Known As | Relation | Record / Tuple | Field / Attribute |

---

# SQL Example

```sql
CREATE TABLE Restaurants (
    RestaurantID INT PRIMARY KEY,
    RestaurantName VARCHAR(100),
    City VARCHAR(50),
    Cuisine VARCHAR(50),
    Rating DECIMAL(2,1)
);
```

### Sample Data

```sql
INSERT INTO Restaurants
VALUES
(101, 'Pizza Hub', 'Surat', 'Italian', 4.5),
(102, 'Burger Point', 'Rajkot', 'Fast Food', 4.2),
(103, 'Spice Villa', 'Ahmedabad', 'Indian', 4.7);
```

---

# Key Points

- A **Table** stores related information about an entity.
- A **Row** represents one complete record in the table.
- A **Column** represents a single attribute of the data.
- Tables, rows, and columns together form the foundation of relational databases in SQL.

---

# Conclusion

In a food delivery application like **Zomato**, the **Restaurants** table stores restaurant information. Each **row** contains the details of one restaurant, while each **column** stores a specific type of information such as the restaurant name, city, cuisine, or rating. Understanding these three concepts is fundamental to working with SQL databases effectively.