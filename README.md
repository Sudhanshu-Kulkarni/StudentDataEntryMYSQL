# Student Management System - Java + MySQL

This project is a simple **Student Management System** implemented in Java that connects to a MySQL database. It allows users to add, update, delete, and search for student records using a command-line interface.

## Features
- Add a new student (Name + PRN)
- Display all students
- Search student by PRN
- Search student by Name
- Search student by Position (based on PRN order)
- Update student name using PRN
- Delete a student record
- Input validation using custom exception (`InvalidChoiceException`)


## Database Setup
1. Create a database named `studentdb` in MySQL.
2. Create a table named `students`:

```sql
CREATE TABLE students (
    name VARCHAR(100),
    prn BIGINT PRIMARY KEY
);
```

3. Update the `DBConnection` class with your MySQL username and password:
```java
String user = "your_mysql_username";
String password = "your_mysql_password";
```

## Project Structure

### Main.java
- Contains the main method and user interface logic.
- Displays a menu and handles user input.
- Uses `StudentOperations` to perform actions.

### Student.java
- A POJO class representing a student.
- Has fields `name` and `prn`.
- Includes getters, setters, and a display method.

### StudentOperations.java
- Handles all CRUD operations on the `students` table.
- Uses JDBC to connect and execute SQL queries.

### DBConnection.java
- Utility class to establish a connection with the MySQL database.

### InvalidChoiceException.java
- Custom exception class for handling invalid menu choices.

## How to Run
1. Ensure MySQL is running and the database/table is created.
2. Compile all Java files:
```bash
javac *.java
```
3. Run the program:
```bash
java Main
```
