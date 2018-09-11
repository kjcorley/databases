>1. What data types do each of these values represent?

"A Clockwork Orange" - string
42 - integer
09/02/1945 - date
98.7 - float
$15.99 - money

>2. Explain when a database would be used. Explain when a text file would be used.

A database is best used for data that needs to be easily queried and changed by multiple instances of an application at the same time.  A text file can be useful for read-only sets of data that will not need to be changed.

>3. Describe one difference between SQL and other programming languages.

SQL is a declaritive programming language meaning the syntax is written describing the desired result.  Other programming languages can be procedural meaning the syntax is used to express how something is done and the result is implicit.

>4. In your own words, explain how the pieces of a database system fit together at a high level.

A database system takes a query and interprets it to read or manipulate data inside the database.  The database engine determines how best to performs these tasks.  The database stores the data in a binary format but in a structure that allows quick reading and writing of data.

>5. Explain the meaning of table, row, column, and value.

A table is a data set that consists of rows and columns filled with values.  Values are the individual pieces of data.  Columns contain data of the same type.  Rows contain data that is related to each other.  For example, all data for a specific user would be in a row, while the user IDs of all users would be in a column.  All of this data would be stored inside a table. 

>6. List three data types that can be used in a table.

string
integer
float

>7. Given this payments table, provide an English description of the following queries and include their results:

     SELECT date, amount
     FROM payments;

Find all dates and amounts in the payment table.  This will return the following:

---

| date                     | amount    |
| ------------------------ | --------- |
| 2016-05-01T00:00:00.000Z | 1500.0000 |
| 2016-05-10T00:00:00.000Z | 37.0000   |
| 2016-05-15T00:00:00.000Z | 124.9300  |
| 2016-05-23T00:00:00.000Z | 54.7200   |

---


     SELECT amount
     FROM payments
     WHERE amount > 500;

Find amounts in the payment table that are greater than 500.  This will return the following:

---

| amount    |
| --------- |
| 1500.0000 |

---



     SELECT *
     FROM payments
     WHERE payee = 'Mega Foods';


Select all data from payments table for the payee 'Mega Foods'.  This will return the following:

---

| amount   |
| -------- |
| 124.9300 |

---


>8. Given this users table, write SQL queries using the following criteria and include the output:

>The email and sign-up date for the user named DeAndre Data.

---

    SELECT email, signup
    FROM users
    WHERE name = 'DeAndre Data';

| email             | signup                   |
| ----------------- | ------------------------ |
| datad@comcast.net | 2008-01-20T00:00:00.000Z |

---

>The user ID for the user with email 'aleesia.algorithm@uw.edu'.

---

    SELECT userid
    FROM users
    WHERE email = 'aleesia.algorithm@uw.edu';

| userid |
| ------ |
| 1      |

---


>All the columns for the user ID equal to 4.

---

    SELECT *
    FROM users
    WHERE userid = 4;

| userid | name           | email             | signup                   |
| ------ | -------------- | ----------------- | ------------------------ |
| 4      | Brandy Boolean | bboolean@nasa.gov | 1999-10-15T00:00:00.000Z |

---
