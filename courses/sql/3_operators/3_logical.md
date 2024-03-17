# Logical

Creates conditional expressions that returns a boolean value (TRUE or FALSE).

We can find ALL, AND, ANY, BETWEEN, EXISTS, IN, LIKE, NOT, OR, IS NULL.


The most used logical operators are : AND, OR, NOT. 

These can be found everywhere within Information Technology.


## And

Checks if all the conditions of the clause are true, retrieving the row(s) in the result set.


```sql
WHERE CONDITION1 AND CONDITION2 AND CONDITIONN;
```

### And Example

```sql
-- Both conditions are TRUE, so 1 record will be shown
SELECT * FROM employee WHERE 1 = 1 AND first_name = 'Manuel';
```

```sql
-- Only first condition is TRUE, so no records will be deleted
DELETE FROM employee WHERE last_name = 'Gentile' AND first_name = 'Joe';
```


## Or

Checks if at least one of the conditions of the clause are true, retrieving the row(s) in the result set.

```sql
WHERE CONDITION1 OR CONDITION2 OR CONDITIONN;
```

### Or Example

```sql
-- Only the second condition is TRUE, so 1 record will be shown
SELECT * FROM employee WHERE 1 = 2 OR first_name = 'Manuel';
```

```sql
-- Both conditions are TRUE, so 2 records will be deleted
DELETE FROM employee WHERE last_name = 'Gentile' OR first_name = 'Joe';
```


## Not

It’s used to negate a condition, so it returns false if the condition is true whilst it returns false if the condition if true.

```sql
WHERE NOT CONDITION1;
```

### Not Example

```sql
-- Only 1 record will be shown
SELECT * FROM employee WHERE NOT (first_name = 'Manuel');
```

```sql
-- All products with a price smaller than 0,01 AND a category different from music will be labelled as useless
UPDATE product SET label = 'useless' WHERE NOT (price > 0,01 OR category='music');
```


## All

The ALL operator is used to compare a column or a value to a set of values returned by a subquery.

It must be preceded by a comparison operator (=, >, >=, <, <=, <>) and it checks if the condition is true for all the values in the result set of the mentioned subquery.

```sql
WHERE COLUMN1 COMPARISON_OPERATOR ALL (subquery);
```

### All Example

```sql
-- This will extract all the products having a price greater than the biggest music product value
SELECT * FROM product 
WHERE price > ALL ( 
    SELECT price FROM product WHERE category='music' 
);
```

```sql
-- This will extract all the products having a price less than the smallest music product value
SELECT * FROM product
WHERE price < ALL (
    SELECT price FROM product WHERE category='music'
);
```


## Any

The ANY operator is used to compare a column or a value to a set of values returned by a subquery.

It must be preceded by a comparison operator (=, >, >=, <, <=, <>) and it checks if the condition is true for any of the values in the result set of the mentioned subquery.

```sql
WHERE COLUMN1 COMPARISON_OPERATOR ANY (subquery);
```

### Any Example

```sql
-- This will extract all the products having a price greater than the smallest music product value
SELECT * FROM product 
WHERE price > ANY ( 
    SELECT price FROM product WHERE category='music' 
);
```

```sql
-- This will extract all the products having a price less than the greatest music product value
SELECT * FROM product
WHERE price < ANY (
    SELECT price FROM product WHERE category='music'
);
```


## Between

The BETWEEN operator is used to compare a column or a value to a range of values. 

It can be used with numerics, chars and dates.

```sql
WHERE COLUMN1 BETWEEN VALUE1 AND VALUE2;
```

### Between Example

```sql
-- This will extract all the products having a price greater than 1 AND smaller than 10
SELECT * FROM product WHERE price BETWEEN 1 AND 10;
```

```sql
-- This will delete all the employees having a letter of name starting from A to N
DELETE FROM employee WHERE first_name BETWEEN 'A' AND 'N';
```


## Exists

The EXISTS operator checks the existence or not of a column or a value to a result set of rows of a subquery.

```sql
WHERE COLUMN1 EXISTS (subquery);
```

### Exists Example

```sql
-- The country table is empty, so no records will be extracted from employee
SELECT * FROM employee
WHERE EXISTS (
    SELECT * FROM country
);
```

```sql
-- The country table is empty, so all records will be deleted from employee
DELETE FROM employee
WHERE NOT EXISTS (
    SELECT * FROM country
);
```


## In

The IN operator is used to compare a column or a value to a set of values returned by a subquery or a comma separated list.

Retrieves the rows in case of matching the value in the set.

It works like having different OR conditions.

```sql
WHERE COLUMN1 IN (subquery | list);
```
corresponds to 
```sql
WHERE COLUMN1 = value1 OR COLUMNN = valueN;
```

### In Example

```sql
-- This will extract all the employees having first name equals to Manuel OR Joe
SELECT * FROM employee WHERE first_name IN ('Manuel','Joe');
```

```sql
-- This will extract all the products having a price equal to the values of the list
SELECT * FROM product WHERE price IN (1,5,10,100);
```


## Like

The LIKE operator is used to compare a CHAR or VARCHAR data type column to another one, a quoted string or a pattern.

It allows to use wildcard characters as **%**, **_**, **[ ]**, **[^]**

```sql
WHERE COLUMN1 LIKE pattern;
```
corresponds to
```sql
WHERE COLUMN1 = value1 OR COLUMNN = valueN;
```

### Like Wildcard

| Wildcard                   | Description                                           |
|----------------------------|-------------------------------------------------------|
| %                          | It represent a sequence of 0 or more chars            |
| _                          | It represent a single char                            |
| [charlist]                 | It represents any single char within a charlist       |
| [^charlist] or [!charlist] | It represents any single char other than the charlist |

### Like Example

```sql
-- This will extract all the employees which first name starts with M
SELECT * FROM employee WHERE first_name LIKE 'M%';
```

```sql
-- This will delete all the employees which first name contains an X
DELETE FROM employee WHERE first_name LIKE '%X%';
```


## Is Null

The IS NULL operator is used to compare whether a column has a null value (TRUE) or not (FALSE).

It works like having different OR conditions.

```sql
WHERE COLUMN1 IS NULL;
```

### Is NUll Example

```sql
-- This will extract all the products having a price set
SELECT * FROM product WHERE price IS NOT NULL;
```

```sql
-- This will delete all the products having a price not set
DELETE FROM product WHERE price IS NULL;
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
