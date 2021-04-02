#Project: Data Warehouse with AWS
Completed by Ken Jung, as part of the Udacity Data Engineering Nanodegree Program

###Introduction
Task is to build an ETL Pipeline that extracts their data from S3, staging it in Redshift and then transforming data into a set of Dimensional and Fact Tables for their Analytics Team to continue finding Insights to what songs their users are listening to. Data is from the two public s3 buckets provided by the Udacity team. One contains information about songs and artst, and the other one has information about log actions done by users. 

###Instruction
Create Table Schema

- Write a SQL CREATE statement for each of these tables in sql_queries.py
- Complete the logic in create_tables.py to connect to the database and create these tables
- Write SQL DROP statements to drop tables in the beginning of create_tables.py if the tables already exist. This way, you can run create_tables.py whenever you want to reset your database and test your ETL pipeline.
- Launch a redshift cluster and create an IAM role that has read access to S3.
- Add redshift database and IAM role info to dwh.cfg.
- Test by running create_tables.py and checking the table schemas in your redshift database.

###Project Workspace and Files
- create_tables.py : Script to drop old table if exists and recreate a new table schema
- dwh.cfg : File that contains configuration information to access Redshift, IAM, and S3
- etl.py : Script that is used for executing the queries that extract JSON data from the S3 bucket and integrate them to a deployed Redshift
- sql_queries.py : Script that contains SQL statement to create, drop, copy, and insert information according to a set schema