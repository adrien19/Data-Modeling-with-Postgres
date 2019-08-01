# Project - Data Modeling with PostgreSQL for Sparkify

A startup called Sparkify wants to analyze the data they've been collecting on songs and user activity on their new music streaming app. The analytics team is particularly interested in understanding what songs users are listening to. Currently, they don't have an easy way to query their data, which resides in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.

The project illustrates how to apply data modeling with Postgres to build an ETL pipeline using Python. In this project, a star schema was used where fact and dimension tables have been defined for a particular analytic focus. The ETL pipeline is used to transfer data from files in two local directories into the fact and dimension tables in Postgres using Python and SQL.


## Getting Started

The details below will get you a summary of the project's database schema for development and testing purposes.

### Prerequisites
Create a file called "dbonfig.cfg" where the host, dbname, user, and password should reside. These will be parsed by ConfigParser.

Before running etl.ipynb or etl.py, make sure create_tables.py has been run at least once to create the sparkifydb, which these other files connect to.


### Installing

All files can be downloaded and stored on local machine. From there, the create the database by running create_tables.py. Then you can either run the etl.ipynb or etl.py. etl.ipynb reads and processes a single file from song_data and log_data and loads the data into your tables. This notebook contains detailed instructions on the ETL process for each of the tables. Whereas, etl.py reads and processes files from song_data and log_data and loads them into your tables. This was created based on your work in the ETL notebook.

files included:
* test.ipynb
* create_tables.py
* etl.ipynb
* etl.py
* sql_queries.py
* README.md
* datasets: song_data and log_data

## Running the tests

Before running test.ipynb, the db credentials must are added appropriately.

Run test.ipynb to confirm the creation of your tables with the correct columns. Make sure to click "Restart kernel" to close the connection to the database after running this notebook.

Example query:

 SELECT * FROM users WHERE users.level='free' LIMIT 5;

Results:

|user_id| first_name| last_name|  gender| level|
|-------|-----------|----------|--------|------|
|26	    |Ryan	    |Smith     |	M	|free  |
|50	    |Ava	    |Robinson  |	F   |free  |
|101    |Jayden     |Fox	   |    M	|free  |
|63	    |Ayla	    |Johnson   |	F   |free  |
|32	    |Lily	    |Burns     |	F	|free  |



## Authors

* **Adrien Ndikumana** - *Initial work* - [adrien19](https://github.com/adrien19)


## Acknowledgments

* With help from Udacity Team
