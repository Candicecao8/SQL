# Create Databases and Tables

*Resources:* 


### Databases!
* Start the CLI: ```mysql-ctl cli;```
* List available databases: ```show databases;```
* Create databases: ```CREATE DATABASE <name>;```
* Drop databases: ```DROP DATABASE <name>;```
* Use databases: ```USE <db_name>;```
* Show which database we are using now: ```SELECT database()```

*Reminder: Be sure to include ```;``` at the end of each command*


### Tables!
A database is a bunch of tables

* Data types: When we create a table, we need to specify the data types. Each column needs to have identical data type
* E.G., ```INT``` (numeric), ```varchar``` (a variable-length string), e.g., ```varchar(100)``` means a string with no more than 100 characters.

**CODE**
* Create tables and specify data types

``` 
CREATE TABLE <tablename> (
    column_name data_type,
    column_name data_type
    );
```
* List tables: ``` SHOW TABLES;```
* Show the contents of the table: ```SHOW COLUMNS FROM <tablename>;``` OR use describe ```DESC <tablename>``` 
* Deleting tables: ```DROP TABLE <tablename>;```


