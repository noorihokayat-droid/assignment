## <center><h1> SESSION -5 : WHERE CLAUSE + LIKE </h1></center>

# TASK - 1 : Create a table called Restaurants with columns: id, name, cuisine, rating, and city. Insert at least 5 sample records representing real or fictional restaurants you might find on Zomato.

**step - 1 : create the restaurant table**

    create table restaurants
	(
        id int AUTO_INCREMENT PRIMARY KEY,
        name varchar(255),
        cuisine varchar(255),
        rating decimal(2,1),
        city varchar(255)
       );

**step - 2 : Insert records**

    insert into restaurants(id,name,cuisine,rating,city)values(1, 'Domino’s Pizza', 'Italian', 4.2, 'Rajkot'),(2, 'Subway', 'Fast Food', 4.5, 'Ahmedabad'),(3, 'McDonald’s', 'American', 3.8, 'Mumbai'),(4, 'Kathiyawadi Rasoi', 'Gujarati', 4.5, 'Rajkot'),(5, 'Spice Garden', 'Indian', 4.3, 'Delhi');

![alt text](<Screenshot 2026-08-16 181610.png>)

# TASK - 2 : Write a SQL query to find all restaurants in the Restaurants table that have a rating greater than 4.0 and are located in either 'Ahmedabad' or 'Surat'.

    SELECT * FROM Restaurants WHERE rating > 4.0 AND (city LIKE '%ahmedabad' OR city LIKE '%surat');

![alt text](<Screenshot 2026-08-16 182746.png>)

# TASK - 3 : Using the LIKE operator, write a query to select all restaurants whose names start with 'Swa' (for example, 'Swagat', 'Swadisht') from the Restaurants table.<br><br><em><strong>Hint:</strong> Use LIKE 'Swa%'.</em>

    SELECT * FROM restaurants WHERE NAME LIKE'SWA%';    

![alt text](<Screenshot 2026-08-16 184356.png>)


# TASK - 4 : Write a SQL query using the BETWEEN keyword to find all restaurants in the Restaurants table with a rating between 3.5 and 4.5 (inclusive).

    SELECT * FROM `restaurants` WHERE rating BETWEEN 3.5 AND 4.5 ;

![alt text](<Screenshot 2026-08-16 191606.png>)


# TASK - 5 : Write a query to find all restaurants whose cuisine is either 'Chinese', 'Italian', or 'South Indian' using the IN operator.

    SELECT * FROM `restaurants` WHERE CUISINE IN ('CHINESE','ITALIAN','SOUTH INDIAN');

![alt text](<Screenshot 2026-08-16 192108.png>)