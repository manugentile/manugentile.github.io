<p align="right"><a href="https://manugentile.github.io/courses/sql/">Back to SQL Course</a> - <a href="https://manugentile.github.io/courses/sql/2_command-types/">Back to Command Types</a></p>


# Data Control Language

It's used for access the stored data.

Commands are GRANT and REVOKE.

## Grant

It's used to provide access or privileges on the database objects
to the users.

```sql
GRANT <privilegeName>
ON <objectName>
TO {<userName> | <roleName>};
```


## Revoke

It's used to revoke access or privileges on the database objects to
the users.

```sql
REVOKE <privilegeName>
ON <objectName>
FROM {<userName> | <roleName>};
```


## Privileges

| Privilege | Description |
|-----------| ----------- |
| SELECT|select statement on the table|
| INSERT|insert statement on the table|
| UPDATE|update statement on the table|
| DELETE|delete statement on the table|
| INDEX|create an index on the table|
| CREATE|create table statement| 
| ALTER|alter table statement|
| DROP|drop table statement|
| ALL|grant all privileges except for GRANT|
| GRANT|allow to grant / manage privileges|



### Grant Example

```sql
-- single privilege to a single user with db
GRANT SELECT
ON employee
TO manuel@localhost;
```

```sql
-- multiple privileges to a single user
GRANT SELECT, INSERT, UPDATE, DELETE
ON employee
TO manuel;
```

```sql
-- all privileges to a single role with db
GRANT ALL
ON employee
TO dev@localhost;
```


### Revoke Example

```sql
-- single privilege to a single user with db
REVOKE SELECT
ON employee
FROM manuel@localhost;
```

```sql
-- multiple privileges to a single user
REVOKE SELECT, INSERT, UPDATE, DELETE
ON employee
FROM manuel;
```

```sql
-- all privileges to a single role with db
REVOKE ALL
ON employee
FROM dev@localhost;
```


<p align="right"><a href="https://manugentile.github.io/courses/sql/">Back to SQL Course</a> - <a href="https://manugentile.github.io/courses/sql/2_command-types/">Back to Command Types</a></p>



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