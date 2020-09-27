# SQL Basics

   This site seeks to introduce the basics of SQL (or Standard Query Language). The goal of this site serves as a reference source for those (myself included) who needs to recall some of the basic concepts in SQL. It also serves as a learning site for those who want to pick up basics of SQL quickly.

   You'll need to have a database server and a client tool to connect to your database installed on your computer to run the codes. In the code examples, I'll be using PostgreSQL, a free and open-source database, though you are free to use other relational database products such as MySQL. The majority of SQL codes in the notebooks on this site should work similarly on other SQL-compliant databases. 

### Why Learn SQL?

   If you are going to work with a relational database, you will need to know how to interact with the data in your database. Albeit you maybe using a tool that generates SQL for you, there may be times when you need to bypass the automatic generation feature and write your own SQL statements. 

   
### Installing PostgreSQL

   At the time of this writing, the latest version of PostgreSQL is 12. PostgreSQL works on major operating systems - Windows, macOS and popular Linux variants including Red Hat and Ubuntu. To install PostgreSQL on your computer, refer to the official site [here](https://www.postgresql.org/download/) and follow the instructions dedicated for your operating system. For client tools, the PostgreSQL installation package already includes psql, a terminal-based front-end for PostgreSQL database. For GUI-based client tools, there are several options available, amongst which is pgadmin4, a popular choice which you can download from the official site [here](https://www.pgadmin.org/download/)


### Sample Database

   To facilitate the learning process, I'll be using a sample DVD rental database for PostgreSQL, which can be obtained from this site [here](https://www.postgresqltutorial.com/postgresql-sample-database/). You can download the sample database and load it onto your database server. 
   

## Contents:

   The basic concepts you'll need to write SQL statements are organised in the following chapters, in the form of Jupyter Notebooks, hosted on GitHub:
   
   + [Querying Data](https://github.com/colintwh/sql-basics/blob/master/querydata.ipynb)
   + [Filtering Data](https://github.com/colintwh/sql-basics/blob/master/filterdata.ipynb)
   + [Querying Multiple Tables](https://github.com/colintwh/sql-basics/blob/master/multijoin.ipynb)
   + *work in progress..*
   
   
---

### Configuring Jupyter Notebooks as an SQL-client tool

   To demonstrate the running of SQL examples, I have configured to use these Jupyter Notebooks to execute SQL statements directly. To begin, you'll need to install `ipython-sql` and import `sqlalchemy` module in your environment which you have launch Jupyter Notebook from. You will also need to install the required DBAPI (shorthand for *Python Database API Specification*) package to connect to your database server. As I'll be using PostgreSQL, the `psycopg2` DBAPI package is thus needed. You can refer to this site [here](https://docs.sqlalchemy.org/en/13/core/engines.html) for more details.
   
   
### Running SQL statements

   In order to run SQL codes on this Jupyter Notebook, I've first created the engine needed to connect to the database. This will be required only once per connection string - meaning you won't have to do it each time when making a connection. The engine is the starting point for any SQLAlchemy application. The general structure of how the SQLAlchemy application connects to the database can be illustrated as follows:

![alt text](https://docs.sqlalchemy.org/en/13/_images/sqla_engine_arch.png)

Following are the steps needed to setup connection to the database from the Jupyter NoteBook (you need to replace the parameters within the `sqlalchemy.create_engine()` method to suit to your own database connection):
   
    !pip install ipython-sql
    !pip install psycopg2

    import sqlalchemy
    sqlalchemy.create_engine('postgresql://postgres:password@localhost/mydatabase')
    
