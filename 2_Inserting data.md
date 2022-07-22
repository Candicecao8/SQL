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
 
 ##

