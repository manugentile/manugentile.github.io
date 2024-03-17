# Data Definition Language

It's used for create and modify the DB structure and its objects.

Commands are CREATE, DROP, ALTER, TRUNCATE and RENAME.


## Create

It's used for creating a database or a table.

```sql
CREATE DATABASE <databaseName>;
```

```sql
CREATE TABLE <tableName> (
    col1 datatype,
    ...
    colN datatype
);
```

### Create Example

```sql
CREATE DATABASE dbTest;
```

```sql
CREATE TABLE employee (
    ID number(18,0),
    FIRST_NAME varchar(50),
    LAST_NAME varchar(50)
);
```


## Drop

It's used for dropping a database or a table.

```sql
DROP DATABASE <databaseName>;
```

```sql
DROP TABLE <tableName>;
```

### Drop Example

```sql
DROP DATABASE dbTest;
```

```sql
DROP TABLE employee;
```


## Alter

It's used for altering a table content.

```sql
-- single column modification, adding a new column
ALTER TABLE <tableName> ADD <columnName> <dataType>;
```

```sql
-- multiple columns modification, adding more columns
ALTER TABLE<tableName> ADD (
    <columnName1> <dataType1>,
    ...
    <columnNameN> <dataTypeN>
);
```

```sql
-- single column modification, changing data type definition
ALTER TABLE <tableName> MODIFY <columnName> <newDataTypeDefinition>;
```

```sql
-- single column modification, adding a new column
ALTER TABLE <tableName> ADD <columnName> <dataType>;
```

```sql
-- multiple columns modification, adding more columns
ALTER TABLE<tableName> ADD (
    <columnName1> <dataType1>,
    ...
    <columnNameN> <dataTypeN>
);
```

```sql
-- single column modification, dropping a column
ALTER TABLE <tableName> DROP <columnName>;
```

```sql
-- multiple columns modification, dropping more columns
ALTER TABLE<tableName> DROP (
    <columnName1>,
    ...
    <columnNameN>
);
```

### Alter Example

```sql
ALTER TABLE<tableName> ADD (
    BIRTH_DATE date,
    BIRTH_COUNTRY varchar(50)
);
```

```sql
-- we can always increase the dimension of a column, but can't decrease it
ALTER TABLE employee MODIFY LAST_NAME varchar(100);
```

```sql
ALTER TABLE employee DROP (
BIRTH_DATE,
BIRTH_COUNTRY
);
```


## Truncate

It's used for removing a table content, while keeping the structure.

Performing a select right after will show no records in the table.

```sql
TRUNCATE TABLE <tableName>;
```
Same result of 
```sql
DELETE FROM TABLE <tableName>;
```
but TRUNCATE is faster.

### Alter Example

```sql
TRUNCATE TABLE employee;
```


## Rename

Used to change the name of an existing table, depending on the RDBMS.

```sql
RENAME TABLE <tableName> TO <newTableName>;
```

```sql
ALTER TABLE <tableName> RENAME TO <newTableName>;
```

### Rename Example

```sql
ALTER TABLE employee RENAME TO employees;
```


<hr>

**Let’s connect**

If you want to learn more about the topic, connect or send me a DM.

<p align="left">
	<a href="https://www.github.com/manugentile" target="_blank" rel="noreferrer">
		<picture>
			<source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/socials/github-dark.svg" />
			<source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/socials/github.svg" />
			<img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/socials/github.svg" width="32" height="32" />
		</picture>
	</a>
	<a href="https://www.linkedin.com/in/manuel-gentile" target="_blank" rel="noreferrer">
		<picture>
			<source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/socials/linkedin-dark.svg" />
			<source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/socials/linkedin.svg" />
			<img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/socials/linkedin.svg" width="32" height="32" />
		</picture>
	</a>
    <a href="https://manugentile.github.io/" target="blank">
        <img src="https://raw.githubusercontent.com/manugentile/manugentile/main/assets/globe-solid.svg" alt="Website" width="30px" />
    </a>

</p>
