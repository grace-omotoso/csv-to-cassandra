## Project: Data Modeling with Cassandra
A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analysis team is particularly interested in understanding what songs users are listening to. Currently, there is no easy way to query the data to generate the results, since the data reside in a directory of CSV files on user activity on the app.

They'd like a data engineer to create an Apache Cassandra database which can create queries on song play data to answer the questions. The data engineer's role is to create a database for this analysis. The database will be tested by running queries provided by the analytics team from Sparkify to create the results.

The data engineer will need to model the data by creating tables in Apache Cassandra to run queries. 

### ETL Pipeline for Pre-Processing csv files
CSV files from the event_data directory should be merged into a single csv file. Data will be loaded into various cassandra tables using this single file. Some columns are exluded from the csv file. The column headers of the csv file that will be used to populate cassandra are:

-   artist
-   firstName of user
-   gender of user
-   item number in session
-   last name of user
-   length of the song
-   level (paid or free song)
-   location of the user
-   sessionId
-   song title
-   userId

The screenshot of sample rows from the file is displayed below:
![Event File Sample Rows](/event_datafile_new.png)



### Creating Apache Cassandra database and tables
-   Design tables to answer queries that users are likely to make
-   Write Apache Cassandra CREATE KEYSPACE and SET KEYSPACE statements
-   Develop your CREATE statement for each of the tables to address each question
-  Load the data with INSERT statement for each of the tables
-   Include IF NOT EXISTS clauses in your CREATE statements to create tables only if the tables do not already exist. Also include DROP TABLE statement for each table, this way you can run drop and create tables whenever you want to reset your database and test your ETL pipeline
-   Test by running the proper select statements with the correct WHERE clause

