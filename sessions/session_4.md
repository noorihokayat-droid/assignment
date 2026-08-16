## <center><h1> SESSION - 4 : SELECT STATEMENT BASICS </h1></center>


# TASK - 1 : Create a table named MusicPlaylist with columns: id, song_name, artist, genre, and duration. Insert at least 5 records representing songs from your favorite Spotify playlist, then write a SELECT statement to retrieve all columns for all songs.

    CREATE TABLE PLAYLIST 
    (
        ID int AUTO_INCREMENT primary key,
        SONG_NAME varchar(255),
        ARTIST varchar(255),
        duration int 
    );

insert into playlist(id,song_name,artist,duration)values(null,'Tum hi ho','Arjit singh','romantic',263),(null,'kahani suno 2.0','kaifi khalil,'urdu/hindi',173),(null,'softly','karan aujla','panjabi pop',155),(null,'kesariya','arijit singh','bollywood romantic',268),(null,'Mi Amor','sharn','punjabi',198);

**TABLE CREATED & INSERT**

**TO SHOW ALL STATEMENT OF TABLE**

    SELECT * FROM musicplaylist;

![alt text](<Screenshot 2026-08-13 175713.png>)



# TASK - 2 :Write a SQL query to display only the song_name and artist columns from the MusicPlaylist table, showing just the first 3 records using the LIMIT keyword.

    select song_name ,artist from musicplaylist limit 3;

![alt text](image-2.png)



# TASK - 3 : Suppose you have a table named FoodOrders with columns: id, restaurant, food_item, and order_date. Write a SQL query to list all unique restaurant names where you have placed orders, using the DISTINCT keyword.

    CREATE table foodorders
	(
        id int AUTO_INCREMENT PRIMARY key,
        restaurant_name varchar(255),
        food_item varchar(255),
        order_date date
      );

    INSERT into foodorders(id,restaurant_name,food_item,order_date)VALUES(null,'dominos','pizza','2026-08-01'),(null,'KFC','Burger','2026-08-02'),(null,'Dominos','Pasta','2026-08-03'),(null,'Subway','Sandwich','2026-08-04'),(null,'McDonalds','Fries','2026-08-05');

**ALL DATA :-**

![alt text](<Screenshot 2026-08-13 232313.png>)

**OUTPUT USING DISTINCT KEY**

    SELECT DISTINCT restaurant_name FROM foodorders;  

![alt text](<Screenshot 2026-08-13 233143.png>)

> DOMINO'S only appears only once even though orderd twice due to use of DISTINCT Keyword.



# TASK - 4 : Write a SQL query on the FoodOrders table to select food_item as 'Dish' and order_date as 'Date Ordered', displaying only these two columns with the column aliases in the output.

    select food_item as dish , order_date as date_orderd from foodorders ;

![alt text](<Screenshot 2026-08-13 233805.png>)



# TASK - 5 : You tried running this query: SELECT DISTINCT food_item, restaurant FROM FoodOrders LIMIT 2, but it returns an error or doesn't work as expected. Identify and fix the mistake in the query.<br><br><em><strong>Hint:</strong> Check the correct placement and usage of the LIMIT keyword in SQL syntax.</em>

    SELECT DISTINCT food_item, restaurant FROM FoodOrders LIMIT 2  
        
> ERROR IN SYNTAX... 
> NOW WE CORRECT THE SYNTAX : 

    SELECT DISTINCT food_item, restaurant_name FROM FoodOrders LIMIT 2 ;

![alt text](<Screenshot 2026-08-13 234226.png>)