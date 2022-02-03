# Summary
This project is to solve the data explosion problem for mucis streaming startup Sparkify. 
Right now their data is in S3, in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.
I will build an ETL pipeline that extracts their data from S3, processes them using Spark, and loads the data back into S3 as a set of dimensional tables. 
After this transition from data warehouse to data lake, it is easier for the analytics team of Spark to use the data to find more insights in what songs their users are listening to.



# The Purpose Of This Database 
Sparkify is a fast growing mucis streaming startup. 
Their user base and song database have been growing explosively. The data warehouse only mode can no longer satisfy all the data storage needs and data analytics requests in the company. As a result, they decided to move their data into Data Lake to enable their data analysts and data sciensts team to expolre their data more freely.



# My Database Schema Design and ETL Pipeline
I built an ETL pipeline that extracts song_data and log_data from S3, processes them using Apache Spark, and loads the data back into S3 as a set of dimensional tables.
The data is organized into a star schema with fact and dimension tables.
A star schema is denormalized. Its join-logic is generally simpler than the join logic required to retrieve data from a highly normalized transactional schema since denormalization is easy, queries can be kept simple, and aggregations are fast.



# How to Run The Python Scripts
By type 'python3 etl.py' code in the terminal, the main function will be called first.
Then the spark session will be created. After that data will be extracted from S3.
After that, the data will be processed by process_song_data function and process_log_data function.
Lastly, the processed data will be loaded back to S3.




# An Explanation of The Files In The Repository
dl.cfg incleds the AWS access credentials 
etl.py reads data from S3, processes that data using Spark, and writes them back to S3
README.md provides discussion on your process and decisions


