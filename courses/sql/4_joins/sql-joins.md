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
