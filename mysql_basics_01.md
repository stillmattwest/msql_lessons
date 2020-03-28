# Creating Databases and Tables in MySQL CLI and MySQL Workbench

## Roadmap

- Our Sample Project
- Create Database
- Create Table
- Drop Table
- Drop Schema
- Insert Into

### CREATE DATABASE

```sql
CREATE DATABASE basic_db;
```

### USE DATABASE

```sql
USE basic_db;
```

### CREATE TABLE

```sql
CREATE TABLE users(id INT AUTO_INCREMENT PRIMARY KEY,first_name VARCHAR(120),last_name VARCHAR(120),password CHAR(60));
```

### DROP TABLE

```sql
DROP TABLE users
```

### DROP DATABASE

```sql
DROP DATABASE basic_db
```

### INSERT INTO

```sql
INSERT INTO users(first_name,last_name,password)
VALUES('Ash','West',1234),('Matt','West',5678);
```
