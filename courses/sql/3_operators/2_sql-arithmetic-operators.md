# Types of SQL operators

## Arithmetic Operators

Arithmetic Performs math operation on numerical data, we can find addition, subtraction, multiplication, division and modulus.

### Addition

Performs the addition operation on numerical data. 

``` sql
SELECT OPERAND1 + OPERAND2; 
```

#### Addition Example

``` sql
-- simple sum
SELECT 10 + 20

-- sum between a column and a number
SELECT price + 20 FROM products; 

-- sum between two columns of a table
SELECT price + tax FROM products; 
```

### Subtraction

Performs the subtraction operation on numerical data. 

``` sql
SELECT OPERAND1 - OPERAND2;
```

#### Subtraction Example

``` sql
-- simple subtraction
SELECT 20 - 20; 

-- subtraction between a column and a number
SELECT price - 20 FROM products; 

-- subtraction between two columns of a table
SELECT price - tax FROM products; 
```

### Multiplication

Performs the multiplication operation on numerical data. 

``` sql
SELECT OPERAND1 * OPERAND2;
``` 

#### Multiplication Example

``` sql
-- simple multiplication
SELECT 10 * 20; 

-- multiplication between a column and a number 
SELECT price * 2 FROM products; 

-- multiplication between two columns of a table
SELECT price * quantity from products;

```

### Division

Performs the division operation on numerical data.

``` sql
SELECT OPERAND1 / OPERAND2;
```

#### Division Example

``` sql
-- simple division
SELECT 10 / 2; 

-- division between a column and a number
SELECT price / 2 FROM products; 

-- division between two columns of a table
SELECT price / quantity FROM products; 
```

### Modulus

Returns the remainder of a division operation on numerical data.

``` sql
SELECT OPERAND1 % OPERAND2;
```

#### Modulus Example

``` sql
-- simple modulus, returns 1
SELECT 5 % 2; 

-- modulus between a column and a number
SELECT price % 2 FROM products; 

-- modulus between two columns of a table
SELECT price % tax FROM products; 
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