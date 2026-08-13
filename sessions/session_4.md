## <center><h1>  SESSION - 4 : SELECT STATEMENT BASIC </h1></center>

# TASK - 1 : Create a table named MusicPlaylist with columns: id, song_name, artist, genre, and duration. Insert at least 5 records representing songs from your favorite Spotify playlist, then write a SELECT statement to retrieve all columns for all songs.

    create table musicplaylist(
    id int AUTO_INCREMENT primary key,
    song_name varchar(255),
    artist varchar(255),
    genre varchar(255),
    duration int );
**table created**

        insert into musicplaylist (id,song_name,artist,genre,duration)values(null,'Tum hi ho','Arijit singh','romantic',263),(null,'kahani suno 2.0','kaifi khalil','urdu/hindi',173),(null,'softly','karan aujla','panjabi pop',155),(null,'kesariya','arijit singh','bollywood romantic',268),(null,'Mi Amor','sharn','punjabi',198);