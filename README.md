# ProjectCassandra
Complete a jupyter template in order to ckeck to load csv files to load music database

## Database design
We user Apache Cassandra to load data files. We need to make three querys so we create three tables for each one

###Query 1:  Give me the artist, song title and song's length in the music app history that was heard during sessionId = 338, and itemInSession = 4
    For songs_by_session table, as the primary key, the column sessionId was used as a partition key because the query will filter firt by this column. itemInSession were used as clustering columns to help make up a unique key and filter by it .


###Query 2: Give me only the following: name of artist, song (sorted by itemInSession) and user (first and last name) for userid = 10, sessionid = 182
    For songs_by_user table, as the primary key, userid and sessionId was used as a composite partition key because the query will filter by this columns. itemInSession were used as clustering columns to help make up a unique 

###Query 3: Give me every user name (first and last) in my music app history who listened to the song 'All Hands Against His Own'
    For user_by_song table, as the primary key, song_title was used as a composite partition key because the query will filter by this columns. userId were used as clustering columns to help make up a unique key (user name could not be unique). In this case both columns are a good primary key, but ff one user could listen one song more than once it was to be neccesary add as clustering column sessionId for example.