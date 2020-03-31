# Data Engineering Nano degree - PostgreSQL Data Warehouse

For this project, we were requested to create an ETL project to read JSON files containing data about users and music listening from Sparkify. A data warehouse structure was requested using ***star*** schema.

## Project Execution

The right order to execute this project is:
1. `create_tables.py`
2. `etl.py`


`create_tables.py` is the script in charge of the database creation and tables dropping and creation. `etl.py` is the script that executes the ETL job logic itself. Its job is to iterate the files according to the data directories given, load the JSON files, process the data and save the result on the database. 


### Notebooks - extra

#### `etl.ipynb`
That's just a notebook to explore the operation of the ETL process from a single file point of view. It's not a mandatory execution.


## Tables 


#### **songplays**
This table stores information about songs that were executed by Sparkify users. For each song that was played, a record is created. That's the fact table. The primary key is the songplay_id which is going to be a serial ID

#### **users**
That is the users' dimension table, where will be stored important info like User ID, Name and Gender are going to seat here. The primary key is the user_id, which is provided on the JSON files.

#### **songs**
This table stores information about the songs - It's a dimension. with information about songs. The primary key will be the song_id, provided by the JSON files.

#### **artists**
That table stores artists' data and will be directly by songs. It's a dimension and the primary key is going to be the artist_id, information that is included on the Sparkify's JSON files.

#### **time**
That's another dimension table. It contains detailed information about every timestamp present on *songplays* table. The primary key is going to be start_time.


