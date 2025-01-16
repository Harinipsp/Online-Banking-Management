# Online-Banking-Management
This innovative project introduces a sophisticated Online Banking System, meticulously crafted to streamline processes and enhance user experiences. The synergy of Java and MySQL technologies empowers the system to offer a diverse range of functionalities, demonstrating the profound implications on contemporary banking practices
# MySQL Connector/J Integration 
The Online Banking System leverages MySQL as its relational database management system. To establish connectivity between the Java application and the MySQL database, the MySQL Connector/J(JAR file), a JDBC driver for MySQL, is utilized. Here are the steps to connect JDBC in Appache NetBeans.

# Step 1: Download and Install MySQL Connector/J
Download the MySQL Connector/J: mysql-connector-java:8.0.28from the official MySQL website (MySQL Connector/J Download) and ensure it is included in my project's classpath(Adding that JAR file in the Library).

# Step 2: Adding Required Dependencies
Under Project files, Choose pom.xml file, and add below dependency.
<dependencies>
        <dependency>
            <groupId>mysql</groupId>
            <artifactId>mysql-connector-java</artifactId>
            <version>8.0.28</version>
        </dependency>
</dependencies>
This dependency is for MySQL Connector/J, which is a JDBC (Java Database Connectivity) driver for connecting Java applications to MySQL databases. The version 8.0.28 indicates the desired version of the MySQL Connector/J.

# Step 3: Adding Requirement for SQL
In module-info.java file (Under Source packages-> default package), add requirement for sql - requires java.sql;

# Step 4: Connectivity Check
Under Dependency folder, Check whether the Connector/J file is added properly(JAR file). Then, check the Services Tab for the database that we are going to work with. It can be found by clicking other connection option. 

# Step 5: Queries for Operations
By using suitable queries, the inserting, updating, validating data can be done. 

These are the steps for connecting Our Database with JDBC.

# MySQL Database: Anchoring the system with a reliable and scalable storage solution, housing user data, account details, and comprehensive transaction records. After installing MySql workbench, Under Schema, the required queries can be written.  
Database Schema
The MySQL database plays a pivotal role in managing critical information:
# Database creation Query
•	To create a database – ‘CREATE DATABASE login;’
•	This will create a new database named ‘login’.
Table creation under login DB
•	To create tables under login database - use login
•	This query is used before creating a table. The tables are created only if they know where to create the tables. This is the purpose of that query.
# 1.	Logindetails Table Creation: Repository for user-specific details such as usernames, passwords, email addresses, account number, pin number, balance and contact information. The below query will create the table logindetails with the respective columns.
           create table logindetails
             (
                id INT AUTO_INCREMENT PRIMARY KEY,
                name varchar(50),
                email varchar(100),
                password varchar(100),
                accountNum int,
                pin int,
                bal int,
                mobile varchar(100),
                address varchar(100),
                timestamp DATETIME  )


# 2.	Transaction Table Creation: Captures detailed transaction information, from timestamps to transaction types and amounts. The below query will create the table transaction with the respective columns.
             create table transaction(
                   id INT AUTO_INCREMENT PRIMARY KEY,
                   accountNum int,
                   pin int,
                   ToAccount varchar(50),
                   transactiontype varchar(50),
                   amount int)   
# Viewing Table Content
To view table content:
•	select * from logindetails
•	select * from transaction
