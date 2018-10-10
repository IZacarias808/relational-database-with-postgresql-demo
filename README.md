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
- Structured so that it allows us to identify and access data in relation to another piece of data in another table
- Database is made up of `tables`
  - A table can have many `rows`, also know as `records`
  - A table can have many `columns` with specific data types
  
## Types of relational databases
#### One-to-One
- The simplest kind of relationship is a one-to-one relationship. Suppose you have a list of people’s names, and a list of social security numbers. Each person has only one social security number, and each social security number is linked to one person
- ex.
  - People-Passports (Each person has only one passport from a particular country and each passport is intended for only one person.)
  - Country-Flag (Each country has only one flag and each flag belongs to only one country.)
  - Spousal Relationships (Each person has only one spouse.)
  

![one-to-one](https://i.imgur.com/wEkbLRR.png?2)

equipment.)
#### One-to-Many
- A more complex (but also far more common) type of relationship is one-to-many/many-to-one. For example, if you have a list of works of art and a list of museums, each work of art can only be in one museum at a time, but each museum can have many works of art.
- ex. 
  - People-Addresses (Each person can live at one address, but each address can house one or more people.)
  - Owners-Pets (Each pet has one owner, but each owner can have one or more pets.)
  - Farmer-Equipment (Each piece of farming equipment is owned by one farmer, but each farmer can own many pieces of 

![one-to-many](https://i.imgur.com/PHJcJT6.png?1)

## What is PostgreSQL?
- 1 of many relational database management system(RDBMS)
- MySQL, SQLite, Microsoft SQL Lite Server, MariaDB
- Allows you READ, CREATE, UPDATE, and DELETE using SQL language to access the database

## What is SQL?
- Structured Query Language(SQL) is a programming used to communicate with data stored in the RDBMS.
- Written similar to the English language




