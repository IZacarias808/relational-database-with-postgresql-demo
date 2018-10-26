# Relational Database with Postgres

## What is a database?
- A set of data stored in a computer
- Structured in a way that is easily accessible
  - ex.
    - username
    - password
    - title
    - description
    - prices
    - products
  
## What is a relational database?
- A type of database
- Structured so that it allows us to identify and access data in relation to another piece of data from another table
- Database is made up of `tables`
  - A table can have many `rows`, also know as `records`
  - A table can have many `columns` with specific data types

## What is PostgreSQL?
- 1 of many relational database management system(RDBMS)
- MySQL, SQLite, Microsoft SQL Lite Server, MariaDB
- Allows you READ, CREATE, UPDATE, and DELETE using SQL language to access the database

## What is SQL?
- Structured Query Language(SQL) is a programming used to communicate with data stored in the RDBMS.
- Written similar to the English language

## CRUD Operations
  - 4 basic functionality 
    - **CREATE:** INSERT
    - **READ:** SELECT
    - **UPDATE:** UPDATE
    - **DELETE:** DELETE

## Live Code
### Installation
- Install Postgres for **Mac**(2 ways to install)
  - Option 1: Download through PostgreSQL website https://www.enterprisedb.com/downloads/postgres-postgresql-downloads
    - Select version `9.6.10`
    
  - Option 2: Hombrew `brew install postgres`
  
- Install Postgres for **Windows** https://www.enterprisedb.com/downloads/postgres-postgresql-downloads
  - Select version `9.6.10`
  - Select operating system `Windows x86-64`
  
  
### Accessing PostgreSQL Shell(psql)
- **Windows:** Windows Start Menu Button -> All Programs -> PostgreSQL 9.6 -> SQL Shell(psql)
- **Mac:** Type in `psql` in your terminal

### Create User and Database
- Open up your postgreSQL Terminal
- Create a user with password - https://www.postgresql.org/docs/9.6/static/sql-createuser.html
- Always end statement with `;`
- List all users `\du`
- Create database and attach user to that database - https://www.postgresql.org/docs/9.6/static/sql-createdatabase.html
- Check databases `\l`

### Create a table
- Connect into your newly created database `\c your_database_name;`
- Create a table - https://www.postgresql.org/docs/9.6/static/sql-createtable.html
- PostgreSQL data types - https://www.postgresql.org/docs/9.6/static/datatype.html
- List all tables `\dt`
- Describe table `\d table_name`

### Select/Querying in table
- Select command - https://www.postgresql.org/docs/9.6/static/sql-select.html
- Select all from a table `SELECT * FROM table_name;`
- Should be able to see all columns from your newly created table

### Insert data in table
- Insert data from the table - https://www.postgresql.org/docs/9.6/static/dml-insert.html
- Can select specific colunmn from table `SELECT * FROM table_name WHERE id = 1;`

### Update data in table
- Update data from the table - https://www.postgresql.org/docs/9.6/static/sql-update.html 
- Example use - https://www.tutorialspoint.com/postgresql/postgresql_update_query.htm

### Delete data in table
- Delete data from the table - https://www.postgresql.org/docs/9.6/static/sql-delete.html 
- Example use - https://www.tutorialspoint.com/postgresql/postgresql_delete_query.htm

### Drop Database and User
- Drop database - https://www.postgresql.org/docs/9.6/static/sql-dropdatabase.html
- Drop user - https://www.tutorialspoint.com/postgresql/postgresql_update_query.htm

## Normalization
Database normalization is process used to organize a database into tables and columns.  The idea is that a table should be about a specific topic and that only those columns which support that topic are included. 
  
## Types of relational databases
#### One-to-One
- The simplest kind of relationship is a one-to-one relationship. Suppose you have a list of people’s names, and a list of social security numbers. Each person has only one social security number, and each social security number is linked to one person

![one-to-one](https://i.imgur.com/wEkbLRR.png?2)
![one-to-one-uml](https://i.imgur.com/PVqrj8E.png)


- ex.
  - People-Passports (Each person has only one passport from a particular country and each passport is intended for only one person.)
  - Country-Flag (Each country has only one flag and each flag belongs to only one country.)
  - Spousal Relationships (Each person has only one spouse.)
  




#### One-to-Many
- A more complex (but also far more common) type of relationship is one-to-many/many-to-one. For example, if you have a list of works of art and a list of museums, each work of art can only be in one museum at a time, but each museum can have many works of art.

![one-to-many](https://i.imgur.com/PHJcJT6.png?1)
![one-to-many-uml](https://i.imgur.com/lozOXoX.png)


- ex. 
  - People-Addresses (Each person can live at one address, but each address can house one or more people.)
  - Owners-Pets (Each pet has one owner, but each owner can have one or more pets.)
  - Farmer-Equipment (Each piece of farming equipment is owned by one farmer, but each farmer can own many pieces of equipment.)


#### Many-to-Many
- Lastly, entities can also have a many-to-many relationship. Let’s say you have a list of books, and a list of authors—each book may have one or more authors, and each author may have written multiple books. In this case, you have many books related to many authors.

![many-to-many](https://i.imgur.com/XJQSZje.png?1)

![many-to-many-junction-table](https://i.imgur.com/NwMRbEE.png?1)
![many-to-many-uml](https://i.imgur.com/gev6KEs.png?1)


- ex.
  - Ingredients-Recipes (Each food item can be used in multiple recipes and each recipe requires multiple ingredients.)
  - Doctors-Patients (Each doctor sees many patients and each patient sees many doctors.)
  - Employees-Tasks (Each employee works on many tasks at a time while each task is being worked on by one or more employees.)
  - Customers-Products (Each customer can purchase many products, and each of those products can be purchased by many different customers.)
  
  

## Resources
[PostgreSQL 9.6 Documentation](https://www.postgresql.org/docs/9.6/static/index.html)

[Normalization](https://www.essentialsql.com/get-ready-to-learn-sql-database-normalization-explained-in-simple-english/)

[Relational Database](https://database.guide/the-3-types-of-relationships-in-database-design/)

[Relational Database Design](http://www.ntu.edu.sg/home/ehchua/programming/sql/relational_database_design.html)





