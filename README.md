# SQL Basics

   This site seeks to introduce the basics of the SQL query language. The goal of this site serves as a reference source for those (myself included) who needs to recall some of the basic concepts in SQL. It also serves as a learning site for those who want to pick up basics of programming quickly.

   You'll need to have a database server and a client tool to connect to your database installed on your computer to run the codes. We will be using PostgreSQL, a free and open-source database, though you are free to use other relational database products such as MySQL. The majority of SQL codes in the notebooks on this site should work similarly on other SQL-compliant databases. 

### Why Learn SQL?

   If you are going to work with a relational database, you will need to know how to interact with the data in your database. Albeit you maybe using a tool that generates SQL for you, there may be times when you need to bypass the automatic generation feature and write your own SQL statements. 

   
### Installing PostgresSQL

   At the time of this writing, the latest version of PostgreSQL is 12. PostgreSQL works on major operating systems - Windows, macOS and popular Linux variants including Red Hat and Ubuntu. To install PostgreSQL on your computer, refer to the official site [here](https://www.postgresql.org/download/) and follow the instructions dedicated for your operation system. For client tools, the PostgreSQL installation package already includes psql, a terminal-based front-end for PostgreSQL database. For GUI-based client tools, there are several options available, amongst which is pgadmin4, a popular choice which you can download from the official site [here](https://www.pgadmin.org/download/)


### Sample Database

   To facilitate the learning process, we'll be using a sample DVD rental database for PostgreSQL, which can be obtained from this site [here](https://www.postgresqltutorial.com/postgresql-sample-database/). You can download the sample database and load it onto your database server. 

## Contents:

   The basic concepts you'll need to write SQL statements are organised in the following chapters hosted on GitHub:
   
   + Creating/Populating a Database
   + Query Primer: `SELECT`, `FROM`, `WHERE`, `GROUP BY`, `ORDER BY`
   + Filtering
   + Querying Multiple Tables: `JOIN`
   + Working with Sets
   + Data Generation, Conversion, and Manipulation
   + Grouping and Aggregates
   + Subqueries
   + Conditional Logic
   + Transactions
   + Indexes and Constraints
   + Views
   + Metadata