# Alter Table and CRUD Operations

## Roadmap

1. Alter Table
   - Add Column
   - Drop Column
   - Modify Column
   - Rename Column
2. CRUD - Create, Read, Update, Delete
   - Insert Into
   - Select
   - Update
   - Delete

## Alter Table

Alter table allows you to modify existing tables by adding, removing, or changing columns. Note that Alter Table isn't for changing _rows_ of data (ie, individual records) it is for changing _columns_ of data (the types of records that can be stored in the table.)

### Add Column

In this example we're going to add an email column to our users table in basic_db.

```sql
ALTER TABLE users
ADD COLUMN email varchar(255)
```

### Drop Column

Drop Column will remove a column from your table, so if we wanted to remove the email column we would do so like this:

```sql
ALTER TABLE users
DROP COLUMN email
```

### Modify Column

We can modify a column by changing its datatype or by renaming it.

Let's say we wanted to give users more characters to use in their email address.

```sql
ALTER TABLE users
MODIFY COLUMN email varchar(300)
```

### Rename Column

Now let's change the column name to email_address

```sql
ALTER TABLE users
RENAME COLUMN email TO email_address
```

## CRUD Operations

All databases can perform CRUD operations (Create, Read, Update, Delete) and many web applications are basically just user interfaces for performing these operations on various types of data. For example, on a social media site users are basically creating posts, reading other people's posts, editing their own posts, and removing that post they _really_ wish they hadn't put up at 3am last night.

### Create

We create rows by using the **INSERT INTO** statement we covered in an earlier lesson. Just to review, if we wanted to add a row to our posts table we would do that like so:

```sql
INSERT INTO posts(title,body,user_id)
VALUES('Training Techniques','If you can dodge a wrench you can dodge a ball!',2);
```

### Read

We read data using the **SELECT** statement. Being able to write a good select statement in a complex database is one of the most important SQL skills to master (maybe _the_ most important) and we'll talk more about it later but the basic syntax is below.

```sql
SELECT first_name,last_name
FROM users
```

### Update

We can update an existing table row with the **UPDATE** statement. Update requires us to identify what row we are modifying, which is usually found with the SELECT statement or by a column that had a unique constraint. We identify our row with the **WHERE** clause.

```sql
UPDATE posts
SET title= 'Training Methods',body= 'Dodge, dip, duck dive, dodge!'
WHERE id = 2;
```

### Delete

We can delete rows with the (wait for it...) **DELETE** statement. Like with UPDATE, we'll need to use a WHERE clause to idenfity which row we want to remove.

```sql
DELETE FROM posts
WHERE id = 2;
```

## Status Update

At this point you pretty much know how to build databases in MySQL. We've gone over installing MySQL, creating, dropping, and modifying databases, tables, columns, and rows and selecting data.

Next we'll cover the art of the SELECT statement, which is where you'll spend a lot of time when working with back end development.
