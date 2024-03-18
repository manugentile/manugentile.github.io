# Comparison

Compares two different data returning a boolean value (TRUE or FALSE), checking if equal, greater or lesser.


## Equal

Checks if the values of two operands are equal or not, returning a boolean (TRUE, FALSE).


```sql
WHERE OPERAND1 = OPERAND2;
```

### Equal Example

```sql
-- Simple condition, returns TRUE
SELECT * FROM employee WHERE 1 = 1;
```

```sql
-- Condition between a column and a value
SELECT * FROM employee WHERE last_name = 'Gentile';
```

```sql
-- Condition between two columns of a table
SELECT * FROM employee WHERE last_name = first_name;
```


## Not Equal

Checks if the values of two operands are equal or not, returning a boolean (TRUE, FALSE).

```sql
WHERE OPERAND1 != OPERAND2;
```

```sql
WHERE OPERAND1 <> OPERAND2;
```

You can use the two symbols interchangeably.

### Not Equal Example

```sql
-- Simple condition, returns FALSE
SELECT * FROM employee WHERE 1 <> 1;
```

```sql
-- Condition between a column and a value
SELECT * FROM employee WHERE last_name != 'Gentile';
```

```sql
-- Condition between two columns of a table
SELECT * FROM employee WHERE last_name <> first_name;
```


## Greater

Checks if the operand on the left is greater than the operand on the right, returning a boolean (TRUE, FALSE).

```sql
WHERE OPERAND1 > OPERAND2;
```

### Greater Example

```sql
-- Simple condition, returns FALSE
SELECT * FROM employee WHERE 1 > 2;
```

```sql
-- Condition between a column and a value
SELECT * FROM employee WHERE age > 21;
```

```sql
-- Condition between two columns of a table
SELECT * FROM products WHERE max_value > min_value;
```


## Less

Checks if the operand on the left is less than the operand on the right, returning a boolean (TRUE, FALSE).

```sql
WHERE OPERAND1 < OPERAND2;
```

### Less Example

```sql
-- Simple condition, returns TRUE
SELECT * FROM employee WHERE 1 < 2;
```

```sql
-- Condition between a column and a value
SELECT * FROM employee WHERE age < 18;
```

```sql
-- Condition between two columns of a table
SELECT * FROM products WHERE max_value < min_value;
```


## Greater Or Equal

Checks if the operand on the left is greater than or equal to the operand on the right, returning a boolean (TRUE, FALSE).

```sql
WHERE OPERAND1 >= OPERAND2;
```

### Greater Example

```sql
-- Simple condition, returns FALSE
SELECT * FROM employee WHERE 1 >= 2;
```

```sql
-- Condition between a column and a value
SELECT * FROM employee WHERE age >= 21;
```

```sql
-- Condition between two columns of a table
SELECT * FROM products WHERE max_value >= min_value;
```


## Less Or Equal

Checks if the operand on the left is less than or equal to the operand on the right, returning a boolean (TRUE, FALSE).

```sql
WHERE OPERAND1 <= OPERAND2;
```

### Less Example

```sql
-- Simple condition, returns TRUE
SELECT * FROM employee WHERE 1 <= 2;
```

```sql
-- Condition between a column and a value
SELECT * FROM employee WHERE age <= 18;
```

```sql
-- Condition between two columns of a table
SELECT * FROM products WHERE max_value <= min_value;
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
