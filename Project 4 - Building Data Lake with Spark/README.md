Aim of this project is to create an ETL pipeline using the data stored in S3 buckets and process that data into respective Fact and dimentsion tables using spark and then upload the parquet files back to S3.

##Prerequisite

1. Install Python 3.x.
2. Also install conda and pyspark

##Dataset (Public S3 buckets): Song Data: s3://udacity-dend/song_data Log Data Path: s3://udacity-dend/log_data

Schema

A Star Schema would be required for optimized queries on song play queries

Fact Table

songplays_table - records in event data associated with song plays i.e. records with page NextSong songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent

Dimension Tables

users_schema_table - users in the app user_id, first_name, last_name, gender, level

songs_schema_table - songs in music database song_id, title, artist_id, year, duration

artists_schema_table - artists in music database artist_id, name, location, lattitude, longitude

time_schema_table - timestamps of records in songplays broken down into specific units start_time, hour, day, week, month, year, weekday

##Pipeline

1.Load the Data which are in JSON Files(Song Data and Log Data) 2.Use Spark to process these JSON files and then generate a set of Fact and Dimension Tables 4.Load back this data to S3

##Execution Steps:

1.Insert your AWS IAM credential in dl.cfg
2.Run etl.py in terminal