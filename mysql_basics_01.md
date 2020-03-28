# Creating Databases and Tables in MySQL CLI and MySQL Workbench

## Roadmap

- Our Sample Project
- Create Database
- Create Table
- Drop Table
- Drop Schema
- Insert Into

## CREATE DATABASE

Create database and create schema do the same thing, which is to add a database to the server. A MySQL server can have any number of databases.

```sql
CREATE DATABASE basic_db;
```

## USE DATABASE

Use database tells MySQL server which database you want to perform operations on.

```sql
USE basic_db;
```

## CREATE TABLE

Databases consist of **tables** which consist of **columns** and **rows**. Create table adds a table to your database.

When you define a table you also need to define colums for it. The columns are the type of data you want the table to store. In the example below we're creating a user table, and each user will have columns for their first and last name as well as a password.

You'll notice we have a lot more going on with **id** than we do with the other columns. Id is the **primary key** for users. A primary key must always be unique, and it can't be a null field (a field without a value.) We've also set id to auto_increment, which will assign id a value automatically whenever a new row is created.

```sql
CREATE TABLE users(id INT AUTO_INCREMENT PRIMARY KEY,first_name VARCHAR(120),last_name VARCHAR(120),password CHAR(60));
```

## DROP TABLE

Drop table removes a table from your database. This results in the loss of all data in that table, so be careful.

```sql
DROP TABLE users
```

## DROP DATABASE

Drop database removes an entire database from your server. Be _extra_ careful.

```sql
DROP DATABASE basic_db
```

## INSERT INTO

Insert into adds **rows** to a table. The rows of a database table are your individual records. So while we defined the types of data (columns) for a user table above, now we are adding the actual users, who will have specific first names, last names, etc.

When you create an insert into statement you can pick and choose which columns you want to add values to, so long as there isn't a constraint that requires you to always fill in a specific column (more on constraints later on.)

So in the example below, if we'd wanted to only fill out last names, leaving first name and password blank, we could have done so simply by leaving those columns out of the statement.

Also note that in the example below we are adding multiple users.

```sql
INSERT INTO users(first_name,last_name,password)
VALUES
('Ash','West',1234),
('Matt','West',5678);
```
