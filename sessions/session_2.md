## <center><h1>Session - 2 : Data Setup + Create Table <h1></center>

## Task-1 : Install MySQL Community Server or SQLite on your system and verify the installation by connecting to the database using the command line or a GUI tool like MySQL Workbench or DB Browser for SQLite.

![alt text](<Screenshot 2026-08-06 182526-1.png>)

![alt text](<Screenshot 2026-08-06 183013.png>)

## Task-2 : Create a new database named 'foodie_app' to simulate a Zomato-style backend.

    create database foodie_app;

## Task-3 : Write a CREATE TABLE statement to define a 'restaurants' table in the 'foodie_app' database

    create table restaurants (
    id int AUTO_INCREMENT PRIMARY key ,
    name varchar(100),
    cuisine varchar(50),
    rating decimal(2,1),
    location varchar(100)
    );

## Task-4 : Design and create a 'users' table for a Flipkart-style app with columns: user_id (primary key), username, email, phone_number, and created_at (date/time). Pick appropriate data types for each column.<br><br><em><strong>Hint:</strong> Think about which columns should be unique and which data types best fit email and phone numbers.</em>

    create table users (
    user_id int AUTO_INCREMENT primary key,
    username varchar(50),
    email varchar(50),
    phone_number varchar(20) UNIQUE,
    created_at datetime
   );

   ![alt text](<Screenshot 2026-08-06 184528.png>)

## Task-5 : Intentionally make a mistake in your CREATE TABLE statement (such as missing a comma or using an unsupported data type), run it, and then fix the error based on the message you receive.

![alt text](<Screenshot 2026-08-06 185159.png>)

![alt text](<Screenshot 2026-08-06 185212.png>)

**<h2>FIX THE ERROR :</h2>** 

![alt text](<Screenshot 2026-08-06 185230.png>)

![alt text](<Screenshot 2026-08-06 185245.png>)