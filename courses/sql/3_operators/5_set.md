# Set

Combines similar type of data from tables mixing the result of queries and returning a single result.

Its operators are UNION, UNION ALL, MINUS, INTERSECT.

## Union

The UNION operator combines the result of two or more tables
in a single result.

The number of columns and their data types must be the same
and in the same order for each SELECT statement.

It doesn’t show duplicated rows.

```sql
SELECT COLUMN1, …, COLUMNn FROM TABLE1
UNION
SELECT COLUMN1, …, COLUMNn FROM TABLE2;
```

### Union Example

```sql
-- It will uniquely extract the country descriptions
SELECT birth_country FROM employee
UNION
SELECT description FROM countries;
```


## Union All

The UNION ALL operator acts like the UNION operator with the only difference that shows duplicated rows.

```sql
SELECT COLUMN1, …, COLUMNn FROM TABLE1
UNION ALL
SELECT COLUMN1, …, COLUMNn FROM TABLE2;
```

### Union All Example

```sql
-- It will extract the country descriptions providing duplicates
SELECT birth_country FROM employee
UNION ALL
SELECT description FROM countries;
```



## Minus / Except

The MINUS (or EXCEPT) operator combines the result of two SELECT statements, simply subtracting the second statement from the first one showing unique records.

```sql
SELECT COLUMN1, …, COLUMNn FROM TABLE1
MINUS
SELECT COLUMN1, …, COLUMNn FROM TABLE2;
```

### Minus Example

```sql
-- It will extract the employees' country descriptions that aren't present in the countries table
SELECT birth_country FROM employee
MINUS
SELECT description FROM countries;
```


## Intersect

The INTERSECT operator combines the result of two SELECT statements in a single result matching the common records.

The number of columns and their data types must be the same and in the same order for each SELECT statement.

It doesn’t show duplicated rows.

```sql
SELECT COLUMN1, …, COLUMNn FROM TABLE1
INTERSECT
SELECT COLUMN1, …, COLUMNn FROM TABLE2;
```

### Intersect Example

```sql
-- It will extract the employees' country descriptions that are present in the countries table
SELECT birth_country FROM employee
INTERSECT
SELECT description FROM countries;
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