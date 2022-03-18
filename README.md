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
To start the project you will need to enter the following command in the root of the project: `docker-compose up`
This will start a PostgreSQL database and a Jupyter Lab with all the dependencies you need to start working with your project (sqalchemy, psycopg2, ipython-sql, pandas..), everything is already setup for you.

`get_started.ipynb` => In this notebook you will find a couple of helper functions:<br>
 - `create_dbs()` will create ,safely, the databases you need to accomplish the task. 
 - `get_db(db_name)` => will return a cursor and a connection to the database you choose. That's everything you need to interact with the db.

There's also a few lines of code to inspire in case you don't know where to start.

## The deliverable

### Python scripts

- create_tables.py: Clean previous schema and creates tables.
- sql_queries.py: All queries used in the ETL pipeline. (optional)
- etl.py: Read JSON and CSV files and load the normalized data into generated tables inside the operational db.
- etl_dw.py: Read from the operational db and transform the data into a star schema inside our datawarehouse.


