# Data Manipulation Language

It's used inserting, updating and deleting data in a DB, so we have `INSERT`, `UPDATE` and `DELETE`.

Before digging into DML commands, let's introduce the most used statement :
```sql
SELECT * FROM <tableName>;
```

This instruction is used for showing data from a table and could be manipulated as well adding other commands, like :
```sql
SELECT * FROM <tableName> WHERE 1=1;
```

```sql
SELECT * FROM <tableName> WHERE 1=1 ORDER BY <columnName>;
```

`SELECT` - clause to extract data from table(s)

`*` (star) - indicates all columns from table(s), otherwise we must specify column(s) we want to extract

`FROM` - clause to retrieve row(s) from the referenced table(s)

`WHERE` - clause to filter record(s), it's optional and could have boolean operators like `AND`, `OR`, `IN`, `LIKE`, `NOT`, etc

`ORDER BY` - clause to order column(s), it's optional

## Insert

It's used for inserting data in a table.

```sql
-- you can define only values of chosen columns
INSERT INTO <tableName> (col1,..., colN) VALUES (val1,...,valN);
```

```sql
-- you must define all columns' values
INSERT INTO <tableName> VALUES (val1,...,valN);
```

```sql
-- bulk insert from a table to another one, selecting or not the colums
INSERT INTO <tableName> (<columns>) SELECT <columns> FROM <anotherTableName>;
```

### Insert Example

```sql
INSERT INTO employee (ID, FIRST_NAME, LAST_NAME) VALUES (1,'Manuel','Gentile');
```

```sql
INSERT INTO employee VALUES (2,'John','Doe');
```

```sql
-- Now, let's assume we have a table called people on the DB having different column names, we can perform a query like that
INSERT INTO employee SELECT IDPEOPLE, FNAME, LNAME FROM PEOPLE;
```


## Update

It's used for modifying data in a table.

```sql
UPDATE <tableName> SET <col1> = <val1>,..., <colN> = <valN> WHERE 1=1;
```

### Update Example

```sql
UPDATE employee SET LAST_NAME = 'Doee' WHERE ID = 2;
```


## Delete

It's used for removing data from a table.

```sql
-- delete all rows
DELETE FROM <tableName>;
```

```sql
-- delete multiple rows
DELETE FROM <tableName> WHERE <col1> = <val1>  ... <operatorN> <colN> = <valN>;
```


### Delete Example

```sql
-- This instruction deletes both rows with ID 1 and 2
DELETE FROM employee
WHERE 1 = 1
AND (LAST_NAME = 'Doee' OR FIRST_NAME = 'Manuel');
```


<hr>

**Let’s connect**

If you want to learn more about the topic, connect or send me a DM.

<p align="left">
	<a href="https://www.github.com/manugentile" target="_blank" rel="noreferrer">
		<picture>
			<img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/socials/github.svg" width="32" height="32" />
		</picture>
	</a>
	<a href="https://www.linkedin.com/in/manuel-gentile" target="_blank" rel="noreferrer">
		<picture>
			<img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/socials/linkedin.svg" width="32" height="32" />
		</picture>
	</a>
    <a href="https://manugentile.github.io/" target="blank">
        <img src="https://raw.githubusercontent.com/manugentile/manugentile/main/assets/globe-solid.svg" alt="Website" width="30px" />
    </a>

</p>