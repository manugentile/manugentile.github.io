<p align="right"><a href="https://manugentile.github.io/courses/sql/">Back to SQL Course</a></p>


# Joins

## [Inner] Join

![](https://raw.githubusercontent.com/manugentile/manugentile.github.io/main/assets/img/inner_join.png)

``` sql
SELECT *
FROM T1
JOIN T2
ON T1.ID = T2.ID;
```

Specifies a join between two tables with an explicit join clause.


It's equal to have a query with WHERE clause.
``` sql
SELECT * FROM T1, T2 WHERE T1.ID = T2.ID;
```

It can be simplified with USING clause.
``` sql
SELECT * FROM T1 JOIN T2 USING (ID);
```

## Left Join

![](https://raw.githubusercontent.com/manugentile/manugentile.github.io/main/assets/img/left_join_1.png)

``` sql
SELECT *
FROM T1
LEFT JOIN T2
ON T1.ID = T2.ID;
```

Specifies a join between two tables with an explicit join clause, preserving unmatched rows from T1 table.


![](https://raw.githubusercontent.com/manugentile/manugentile.github.io/main/assets/img/left_join_2.png)

``` sql
SELECT *
FROM T1
LEFT JOIN T2
ON T1.ID = T2.ID
WHERE T2.ID IS NULL;
```


## Right Join

![](https://raw.githubusercontent.com/manugentile/manugentile.github.io/main/assets/img/right_join_1.png)

``` sql
SELECT *
FROM T1
RIGHT JOIN T2
ON T1.ID = T2.ID;
```

Specifies a join between two tables with an explicit join clause, preserving unmatched rows from T2 table.


![](https://raw.githubusercontent.com/manugentile/manugentile.github.io/main/assets/img/right_join_2.png)

``` sql
SELECT *
FROM T1
RIGHT JOIN T2
ON T1.ID = T2.ID
WHERE T1.ID IS NULL;
```

## Full [outer] Join


![](https://raw.githubusercontent.com/manugentile/manugentile.github.io/main/assets/img/full_join_1.png)

``` sql
SELECT *
FROM T1
FULL [OUTER] JOIN T2
ON T1.ID = T2.ID;
```

Specifies a join between two tables with an explicit join clause, preserving unmatched rows from T2 table.


![](https://raw.githubusercontent.com/manugentile/manugentile.github.io/main/assets/img/full_join_2.png)

``` sql
SELECT *
FROM T1
FULL [OUTER] JOIN T2
ON T1.ID = T2.ID
WHERE T1.ID IS NULL OR T2.ID IS NULL;
```


<p align="right"><a href="https://manugentile.github.io/courses/sql/">Back to SQL Course</a></p>



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