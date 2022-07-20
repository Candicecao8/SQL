# MySQL Tips

## How to get back to MySQL database after a break

1. Start by running the mysql service and opening the mysql shell, this can be done simultaneously with a single command
```
mysql-ctl cli
```
If this worked then you should see `mysql>` in your terminal. You may now enter the following MySQL commands:

2. Open the database you want to use:
```
USE <db_name>
```

## Source a SQL file 

1. Check if you are in the right directory and check for the sql file
``` ls ```

2. Locate the right database
``` USE <db_name>```

3. Make sure to save the sql file first before running any command. Then type in ```source <sql_file_name>``` and run

