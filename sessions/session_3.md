
## <center><h1> SESSION - 3 : INSERT | UPDATE | DELETE</h1></center>

# TASK - 1 :Create a table called Playlist with columns: id (INT, primary key), song_name (VARCHAR), artist (VARCHAR), and duration (INT, seconds). Insert a single row for your current favorite song.

    CREATE TABLE PLAYLIST (
    ID int AUTO_INCREMENT primary key,
    SONG_NAME varchar(255),
    ARTIST varchar(255),
    duration int );

    insert into playlist(id,song_name,artist,duration)values(null,'Tum hi ho','Arjit singh',263);
 
**table created & 1 row inserted**


# TASK - 2 : Insert 3 new rows into the Playlist table for songs you recently listened to on Spotify, including their song_name, artist, and duration.

    INSERT into playlist(id,song_name,artist,duration)values(null,'saza','sheheryar rehan',190),(null,'leher','Arjit singh',115),(null,'sathiya','Darshan Raval',190);

# TASK-3 : Update the artist name for one of your Playlist entries to fix a typo (for example, change 'Arjit Singh' to 'Arijit Singh') using the UPDATE statement with a WHERE clause.

    update playlist set artist='Arijit singh' where ARTIST='arjit singh';

# TASK - 4 : Delete a song from the Playlist table where the duration is less than 120 seconds using the DELETE statement and a WHERE clause.<br><br><em><strong>Hint:</strong> Make sure your WHERE clause is specific so you don’t accidentally delete all rows.</em>

    delete  from playlist WHERE duration < 120 ; 

# TASK - 5 :Write an SQL statement that would update the song_name for all songs by 'AP Dhillon' in your Playlist to add '(Remix)' at the end of the name, but only if the duration is more than 180 seconds.<br><br><em><strong>Constraint:</strong> Combine UPDATE with WHERE to target only the correct rows.</em>

        UPDATE playlist SET song_name = concat(song_name,'(Remix)')where artist='Arijit singh' AND duration>180;

![alt text](<Screenshot 2026-08-09 132803.png>)