# ProjectCassandra
Complete a jupyter template in order to ckeck to load csv files to load music database

## Database design
We user Apache Cassandra to load data files. We need to make three querys so we create three tables for each one

###Query 1:  Give me the artist, song title and song's length in the music app history that was heard during sessionId = 338, and itemInSession = 4
    This query creates music_library

###Query 2: Give me only the following: name of artist, song (sorted by itemInSession) and user (first and last name) for userid = 10, sessionid = 182
    This query creates music_library2

###Query 3: Give me every user name (first and last) in my music app history who listened to the song 'All Hands Against His Own'
    This query creates music_library3