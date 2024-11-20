# Registration_Form
Registration Management System - Backend
This project implements a backend for a Registration Management System using Java, JDBC, and SQL. It includes CRUD operations (Create, Read, Update, Delete) to manage registration records in a database.

Features
Insert a new registration record into the database.
Retrieve and display all registration records.
Update an existing registration record.
Delete a registration record from the database.
Technologies Used
Java (JDK 8+)
JDBC (Java Database Connectivity)
MySQL (or any SQL-compatible database)
Project Structure
mathematica
Copy code
Backend/
├── src/
│   ├── com/
│   │   ├── jlc/
│   │   │   ├── p1/
│   │   │   │   ├── Insert.java
│   │   │   │   ├── Select.java
│   │   │   │   ├── Update.java
│   │   │   │   ├── delete.java
│   │   │   │   ├── JDBCUtil.java
├── README.md
Prerequisites
Install JDK 8+.
Install and configure MySQL.
Add the MySQL JDBC Driver (mysql-connector-java) to your project classpath.
Database Setup
Run the following SQL commands to set up the database and table:

sql
Copy code
CREATE DATABASE RegistrationDB;

USE RegistrationDB;

CREATE TABLE Registration (
    ID INT AUTO_INCREMENT PRIMARY KEY,
    Name VARCHAR(50) NOT NULL,
    Email VARCHAR(100) NOT NULL UNIQUE,
    DateOfBirth DATE NOT NULL,
    PhoneNumber VARCHAR(15) NOT NULL,
    Address VARCHAR(255) NOT NULL,
    RegistrationDate TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
Steps to Run
Clone this repository:
bash
Copy code
git clone https://github.com/<your-username>/RegistrationManagementSystem-Backend.git
cd RegistrationManagementSystem-Backend
Configure your database connection:
Update the database URL, username, and password in the JDBCUtil class.
Compile the Java files:
bash
Copy code
javac -cp .;path/to/mysql-connector-java.jar com/jlc/p1/*.java
Run each operation:
Insert a record:
bash
Copy code
java com.jlc.p1.Insert
Read records:
bash
Copy code
java com.jlc.p1.Select
Update a record:
bash
Copy code
java com.jlc.p1.Update
Delete a record:
bash
Copy code
java com.jlc.p1.delete
Project Limitations
Assumes a running MySQL server.
Basic error handling included but can be improved.
Limited validation of input data.
License
This project is open source and free to use under the MIT License.












