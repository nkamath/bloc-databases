## Checkpoint 1 Exercises

> **What data types do each of these values represent?**

1. "A Clockwork Orange"
A) String.
1. 42
A) Integer.
1.  09/02/1945
A)  Date.
1. 98.7
A) Float.
1. $15.99
A) String

> **Explain when a database would be used. Explain when a text file would be used.**

A) A text file can be used for simple data retrieval procedures where you can guarantee that storage and retrieval will happen without collisions. Once there are more complicated requirements of multiple applications accessing the same data, a database can be used. 

> **Describe one difference between SQL and other programming languages.**

SQL is declarative whereas many common programming languages (like python, javascript) are by nature procedural.

> **In your own words, explain how the pieces of a database system fit together at a high level.**

The database stores the necessary data that's required across application instances. The first piece that users interact with is the program itself. When data is created and needs to be stored, it is usually an API call to the database application. Similarly, when the data needs to be retrieved, it calls another API on the database application. The database application is able to guarantee that operations are performed even if there are multiple client applications sending requests to store or retrieve data.

> **Explain the meaning of table, row, column, and value.**

A table is a collection of data made up of rows and columns. A single entry in the table is a row. The descriptors of the data in the table are the columns. The data for a particular column for an entry in the table is its value.

> **List three data types that can be used in a table.**

Ans) Integer, Float, String

> **Given this payments table, provide an English description of the following queries and include their results:**

```
     SELECT date, amount
     FROM payments;
```
The date and amount for all rows of the payments table.

| date                     | amount    |
| ------------------------ | --------- |
| 2016-05-01T00:00:00.000Z | 1500.0000 |
| 2016-05-10T00:00:00.000Z | 37.0000   |
| 2016-05-15T00:00:00.000Z | 124.9300  |
| 2016-05-23T00:00:00.000Z | 54.7200   |

---

```
     SELECT amount
     FROM payments
     WHERE amount > 500;
```

Outputs all amounts from the payments table that are over 500

| amount    |
| --------- |
| 1500.0000 |

---

```
     SELECT *
     FROM payments
     WHERE payee = 'Mega Foods';
```
All rows from the table where payee is Mega Foods.

| date                     | payee      | amount   | memo      |
| ------------------------ | ---------- | -------- | --------- |
| 2016-05-15T00:00:00.000Z | Mega Foods | 124.9300 | Groceries |

---

> **Given this users table, write SQL queries using the following criteria and include the output:**

**The email and sign-up date for the user named DeAndre Data.**


    SELECT email, signup FROM users
    WHERE name = 'DeAndre Data';

| email             | signup                   |
| ----------------- | ------------------------ |
| datad@comcast.net | 2008-01-20T00:00:00.000Z |

---
**The user ID for the user with email 'aleesia.algorithm@uw.edu'.**

    SELECT userid FROM users
    WHERE email = 'aleesia.algorithm@uw.edu';

| userid |
| ------ |
| 1      |

---

**All the columns for the user ID equal to 4.**

    SELECT * FROM users
    WHERE userid = 4;

| userid | name           | email             | signup                   |
| ------ | -------------- | ----------------- | ------------------------ |
| 4      | Brandy Boolean | bboolean@nasa.gov | 1999-10-15T00:00:00.000Z |

---
