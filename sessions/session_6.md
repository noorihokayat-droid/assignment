## <center><h1> session - 6 : ORDER BY + SORTING </h1> </center>

# TASK - 1 : Write an SQL query to display all products from a 'products' table and sort them by price in ascending order, similar to how Flipkart lists items from lowest to highest price.

    create table products(
    id int AUTO_INCREMENT PRIMARY KEY,
    product_name varchar(100),
    price decimal(10,2)
    );

    INSERT INTO Products (id, product_name, price) VALUES
    (1, 'Pen', 10.00),
    (2, 'Notebook', 50.00),
    (3, 'Headphones', 1200.00),
    (4, 'Mobile Phone', 15000.00),
    (5, 'Laptop', 45000.00),
    (6, 'Smartwatch', 5000.00);

**<h2>Flipkart lists items from lowest to highest price.</h2>**

    SELECT * FROM Products ORDER BY price ASC;

![alt text](<Screenshot 2026-08-16 202512.png>)

# TASK - 2 :Modify your previous query to show the top 5 most expensive products using ORDER BY with DESC and LIMIT.

    SELECT * from products order by price desc limit 3;

![alt text](<Screenshot 2026-08-16 203134.png>)   

# TASK - 3 : Given a 'movies' table with columns 'title', 'release_year', and 'rating', write an SQL query to list all movies sorted first by release_year in descending order (latest first), then by rating in descending order (highest rated first).

    CREATE TABLE Movies (
    id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(100),
    release_year INT,
    rating DECIMAL(2,1)
    );

    INSERT INTO Movies (id, title, release_year, rating) VALUES
    (null, 'Inception', 2010, 8.8),
    (null, 'RRR', 2022, 8.0),
    (null, 'KGF Chapter 2', 2022, 8.4),
    (null, 'Interstellar', 2014, 8.6),
    (null, 'Dangal', 2016, 8.5);

**<h2>1. list all movies sorted first by release_year in descending order (latest first)</h2>**

    SELECT * FROM `movies` order by release_year DESC; 

![alt text](<Screenshot 2026-08-16 204757.png>)

**<h2>2. list all movies sorted by rating in descending order (highest rated first).</h2>**

    SELECT * from movies ORDER BY rating desc ;

![alt text](<Screenshot 2026-08-16 205023.png>)

# TASK - 4 :Write an SQL query to display the first 10 restaurants from a 'restaurants' table, sorted alphabetically by name, just like Zomato's A-Z listing.<br><br><em><strong>Hint:</strong> Use ORDER BY with LIMIT.</em>

    CREATE TABLE Restaurants (
    id INT  AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    cuisine VARCHAR(50),
    rating DECIMAL(2,1),
    city VARCHAR(50)
    );

    INSERT INTO Restaurants (id, name, cuisine, rating, city) VALUES
    (null, 'Domino’s Pizza', 'Italian', 4.2, 'Rajkot'),
    (null, 'Subway', 'Fast Food', 3.5, 'Ahmedabad'),
    (null, 'McDonald’s', 'American', 3.8, 'Mumbai'),
    (null, 'Kathiyawadi Rasoi', 'Gujarati', 4.5, 'Rajkot'),
    (null, 'Spice Garden', 'Indian', 4.3, 'Delhi'),
    (null, 'Swagat', 'Gujarati', 4.4, 'Surat'),
    (null, 'Swadisht', 'Indian', 4.2, 'Ahmedabad'),
    (null, 'Barbeque Nation', 'Multi-Cuisine', 4.1, 'Mumbai'),
    (null, 'Pizza Hut', 'Italian', 4.0, 'Delhi'),
    (null, 'Udupi Palace', 'South Indian', 4.3, 'Bangalore'),
    (null, 'Mainland China', 'Chinese', 4.2, 'Ahmedabad');

**<h2>sorted alphabetically by name, just like Zomato's A-Z listing.</h2>**

    SELECT * FROM `restaurants` ORDER by name ASC LIMIT 10;

![alt text](<Screenshot 2026-08-16 210354.png>)

# TASK - 5 : Suppose you want to display the top 3 trending songs from a 'songs' table based on play_count, but if two songs have the same play_count, the more recently added song should come first. Write the SQL query to achieve this.<br><br><em><strong>Hint:</strong> Use ORDER BY with multiple columns.</em>

    CREATE TABLE Songs (
    id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(100),
    play_count INT,
    added_date DATE
    );

    INSERT INTO Songs (id, title, play_count, added_date) VALUES
    (null, 'Song A', 500, '2026-08-01'),
    (null, 'Song B', 800, '2026-08-10'),
    (null, 'Song C', 800, '2026-08-15'),
    (null, 'Song D', 300, '2026-07-20'),
    (null, 'Song E', 1000, '2026-08-12');   

**<h2>top 3 trending songs</h2>**

    SELECT * FROM Songs ORDER BY play_count DESC, added_date DESC LIMIT 3;

![alt text](<Screenshot 2026-08-16 211644.png>)