# Create Databases and Tables

### Databases!

**CODE**

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





# Inserting data


## Adding data to your tables

``` 
INSERT INTO <tablename> (<column1>, <column2>)
VALUES (<column1_value>, <column2_value);
```

*Multiple Insert*

```
INSERT INTO <tablename>(<column1>,<column2>)
VALUES (<value>,<value>),
       (<value>,<value>),
       (<value>,<value>);
```

*Show warnings*: ``` SHOW WARNINGS;```

## NULL and NOT NULL
* Prevent Null values: When ```CREATE TABLE```, add ```NOT NULL``` after each column. E.g.,
  ```
  CREATE TABLE cats(
      name VARCHAR(50) NOT NULL,
      age INT NOT NULL
      );
  ```
* Set default values: When ```CREATE TABLE```, add ```DEFAULT <default_value> ``` after each column. E.g.,
  ```
  CREATE TABLE cats(
      name VARCHAR(50) DEFAULT 'unnamed',
      age INT DEFAULT 99
      );
  ```
 * Combine ```NOT NULL``` and ```DEFAULT <default_value>```
 
 ## Primary Key:
 A unique identifier.
 
* Set primary key: Add ``` PRIMARY KEY (<key>)``` when ```CREATE TABLE```. E.g.,
  ```
  CREATE TABLE unique_cats(
      cat_id INT NOT NULL,
      name VARCHAR(50),
      age INT,
      PRIMARY KEY(cat_id)
      );
  ```
  * Adding in ```AUTO_INCREMENT```: No longer have to specify the primary key.
    ```
    CREATE TABLE unique_cats2 (
    cat_id INT NOT NULL AUTO_INCREMENT,
    name VARCHAR(100),
    age INT,
    PRIMARY KEY (cat_id)
    );
    ```



# SQL Select Statement Process:


1. Getting Data (```FROM```, ```JOIN```)
* Tip: Use ```ON``` as a condition to get the qualified rows.

2. Row Filter (```WHERE```)
i.e., evaluate every row using conditional expressions. Rows evaluated to true will be reserved.

3. Grouping (```GROUP BY```)
*  After this point, all Select expressions will be evaluated per group, instead of per row.

4. Group Filter (```HAVING```)
*  Processed after the Group by clause. This clause consists of a logical predicate.

5. Return Expression (```SELECT```)
*  The processor will evaluate what will be printed as a result of the query.
* We can use ```AS``` to change column name

6. Order & Paging (```ORDER BY``` & ```LIMIT```/```OFFSET```)
*  Presentation ordering and the ability to limit the size of the result set.


# CRUD: Create, Read, Update, Delete

* Update: ```UPDATE <tablename> SET <updated_command>``` e.g.,

  ```UPDATE cats SET breed = 'Shorthair' WHERE breed = 'Tabby';```
* Delete: ```DELETE FROM <tablename> WHERE <filter>``` e.g.,

  ```DELETE FROM cats WHERE name = 'egg';```









