# Data Warehousing with Postgres

## Introduction
A startup called CodeOp Fintech Solutions S.L., wants to analyze the data they've been collecting on transactions and user activity on their new payments app. The analytics team is particularly interested in understanding where payments are being made. Currently, they don't have an easy way to query their data, which resides in a directory of JSON and CSV logs on transactions activity on the app.

They'd like a data engineer to create a Postgres database with tables designed to optimize queries on transactions analysis, and bring you on the project. Your role is to create a database schema and ETL pipeline for this analysis. You'll be able to test your database and ETL pipeline by running queries given to you by the analytics team from CodeOp and compare your results with their expected results.

## Project Description
In this project, you'll apply what you've learned on data modeling with Postgres and build an ETL pipeline using Python + SQL. To complete the project, you will need to define fact and dimension tables for a star schema for a particular analytic focus, and write an ETL pipeline that transfers data from files in two local directories into these tables in Postgres using Python and SQL.

## Getting started

### Requirements
- Docker
- Docker compose

### The project
To start the project you will need to enter the following command in the root of the project: <br> `docker-compose up` <br>
This will start a PostgreSQL database and a Jupyter Lab with all the dependencies you need to start working with your project (sqalchemy, psycopg2, ipython-sql, pandas..), everything is already setup for you.
Whenever you want to bring down the containers don't forget to `docker-compose down`.

`get_started.ipynb` => In this notebook you will find a couple of helper functions:<br>
 - `create_dbs()` will create ,safely, the databases you need to accomplish the task. 
 - `get_db(db_name)` => will return a cursor and a connection to the database you choose. That's everything you need to interact with the db.

 There's also a few lines of code to inspire in case you don't know where to start.

 Inside the **data/** folder you will find all the files with the data needed to start coding. So the first step will be bring all the data in those files into our operational db in a normalize manner. Once we have our operational db set up we can start the denormalization process to build our datawarehouse.

 Hint: We need to end up with a start schema in our dw.
 Important: The final goal is to create a dw with a star schema so don't lose too much time normalizing the data into the operational db. It is ok if the data is not completely normalize. What it is important is the final result in the datawarehouse which is the purpose of this lesson.



## The deliverable

### Python scripts

- create_tables.py: Creates all the tables.
- sql_queries.py: All queries used in the ETL pipeline. (optional)
- etl.py: Read JSON and CSV files and load the normalized data into generated tables inside the operational db.
- etl_dw.py: Read from the operational db and transform the data into a star schema inside our datawarehouse.


