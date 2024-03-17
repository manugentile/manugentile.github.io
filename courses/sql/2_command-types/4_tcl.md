# Transaction Control Language

It's used for handling the transaction, its commands are COMMIT and ROLLBACK.


## What is a transaction in SQL?

A SQL transaction is a set of one or more SQL statements that
interact with a database and are essential for maintaining
database integrity.

A transaction can be committed or rollbacked (becomes undone)
to a database as a single logical unit.

Transactions are used to preserve integrity when multiple
operations are executed concurrently or when various users
interact concurrently with a database.


## Commit

It's used for saving data permanently on database. 

Once a transaction has been committed, it's not possible to restore its previous state.

<u>It only works on DML commands.</u>

```sql
COMMIT;
```

### Commit Example

Let's assume table employee is empty.

We are going to insert a single row, then we persist data (commit)
and close the session.

Another user opens a new one and selects employee.

The result will be the single row.


```sql
SELECT * FROM employee;
-- no records found
```

```sql
INSERT INTO employee VALUES (1,'Manuel', ‘Gentile');
```

```sql
COMMIT;
-- this user closes the session
```

```sql
-- another user opens the session
SELECT * FROM employee;
-- 1 record found (1,'Manuel', ‘Gentile')
```


## Rollback

It's used for reverting data not persisted on database by a transaction.

Once a transaction has been rollbacked, it's not possible to restore its previous state.

<u>It only works on DML commands.</u>

```sql
ROLLBACK;
```

### Rollback Example

Let's assume table employee is empty.

We are going to insert a single row, then we rollback the transaction data and close the session.

Another user opens a new one and selects employee.

The result will be no records.


```sql
SELECT * FROM employee;
-- no records found
```

```sql
INSERT INTO employee VALUES (1,'Manuel', 'Gentile');
```

```sql
ROLLBACK;
-- this user closes the session
```

```sql
-- another user opens the session
SELECT * FROM employee;
-- no records found
```







<hr>

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
