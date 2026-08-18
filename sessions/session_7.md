## <center><h1> SESSION - 7 : Aggregate Functions </h1></center>

# TASK - 1 : Create a table called Orders with columns: order_id, user_name, total_amount, and order_date. Insert 5 sample rows with different users and order amounts, including at least one NULL value for total_amount.

    create table orders (
        order_id int AUTO_INCREMENT PRIMARY KEY ,
        user_name varchar(255),
        total_amount decimal(10,2),
        order_date date
    )

    INSERT INTO Orders (order_id, user_name, total_amount, order_date) VALUES
    (null, 'Neha', 1200.50, '2026-08-01'),
    (null, 'Rahul', 800.00, '2026-08-02'),
    (null, 'Aarti', NULL, '2026-08-03'),
    (null, 'Karan', 1500.75, '2026-08-04'),
    (null, 'Meera', 950.00, '2026-08-05');

![alt text](<Screenshot 2026-08-18 183432.png>)

# TASK - 2 :Write a SQL query to count how many orders were placed by each user in the Orders table, displaying user_name and the number of orders as order_count.

    select user_name,count(*) AS order_count FROM orders GROUP BY user_name;

![alt text](<Screenshot 2026-08-18 184127.png>)

# TASK - 3 : Write a SQL query to calculate the average total_amount of all orders in the Orders table, making sure to ignore any NULL values.

    SELECT AVG(total_amount) FROM orders ;

![alt text](<Screenshot 2026-08-18 184545.png>)

# TASK - 4 : Suppose you are building a Flipkart-style dashboard: Write a SQL query to find the highest and lowest order amounts (MAX and MIN) from the Orders table, and display both values in a single result row.

    SELECT MAX(total_amount) AS highest_order,MIN(total_amount) AS lowest_order FROM Orders;

![alt text](<Screenshot 2026-08-18 184827.png>)

# TASK - 5 : Write a SQL query to calculate the total sales (SUM of total_amount) for all orders, but only include orders where total_amount is not NULL.<br><br><em><strong>Hint:</strong> Use a WHERE clause to filter out NULL values before applying the SUM function.</em>

    SELECT SUM(total_amount) AS total_sales FROM orders where total_amount is NOT null ;

![alt text](<Screenshot 2026-08-18 185254.png>)