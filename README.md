# Schema for Song Play Analysis

## Purpose  
The purpose of creating the Postfres database is to help Sparkify to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to.

## Database schema design
Using the song and log datasets, I created a star schema optimized for queries on song play analysis. This includes the following tables.

### Fact Table
1.	**songplays** - records in log data associated with song plays i.e. records with page NextSong

•	songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent

### Dimension Tables
1.	**users** - users in the app

•	user_id, first_name, last_name, gender, level

2.	**songs** - songs in music database

•	song_id, title, artist_id, year, duration

3.	**artists** - artists in music database

•	artist_id, name, location, latitude, longitude

4.	**time** - timestamps of records in songplays broken down into specific units

•	start_time, hour, day, week, month, year, weekday

## ETL PROCESS
1.	**Process song_data**
In this first part, I performed ETL on the first dataset, song_data, to create the songs and artists dimensional tables.

2.	**Process log_data**
In this part, I performed ETL on the second dataset, log_data, to create the time and users dimensional tables, as well as the songplays fact table.
