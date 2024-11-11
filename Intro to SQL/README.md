# 🚀 Getting Started
## 1. Setup
Install SQL: If not already installed, use a tool like [SQLite](https://sqlitebrowser.org/dl/) or an online platform such as [DB Fiddle](https://www.db-fiddle.com/) or [SQLBolt](https://sqlbolt.com/).

## 2. The Basics of SQL
🗂️ What is SQL? <br>
**SQL** (Structured Query Language) is a language designed for interacting with databases. It allows you to store, manipulate, and retrieve data. The primary commands are divided into:
* DDL (Data Definition Language): Commands like CREATE, ALTER, DROP.
* DML (Data Manipulation Language): Commands like SELECT, INSERT, UPDATE, DELETE.
* DCL (Data Control Language): Commands like GRANT, REVOKE.

## 📖 Section 1: Data Definition Language (DDL)
### 1. Creating a Table
```sql
CREATE TABLE Students (
    StudentID INTEGER PRIMARY KEY,
    FirstName TEXT,
    LastName TEXT,
    Age INTEGER,
    Major TEXT,
    GPA REAL
);
```
**Explanation**: This command creates a Students table with columns for StudentID, FirstName, LastName, Age, Major, and GPA.

### 2. Dropping a Table
```sql
DROP TABLE IF EXISTS Students;
```
**Explanation**: Deletes the Students table if it exists. Use carefully as it permanently removes the table and data within it.

## 📖 Section 2: Data Manipulation Language (DML)
### 1. Inserting Data
```sql
INSERT INTO Students (StudentID, FirstName, LastName, Age, Major, GPA)
VALUES (1, 'Alice', 'Smith', 20, 'Mathematics', 3.8),
       (2, 'Bob', 'Johnson', 21, 'Computer Science', 3.6),
       (3, 'Charlie', 'Lee', 22, 'Statistics', 3.9);
```
**Explanation**: Adds records into the Students table.

### 2. Updating Data
```sql
UPDATE Students
SET GPA = 3.9
WHERE StudentID = 2;
```
**Explanation**: Updates the GPA of the student with StudentID 2 to 3.9.

### 3. Deleting Data
```sql
DELETE FROM Students
WHERE Age < 21;
```
**Explanation**: Removes all records where the Age is less than 21.

## 📖 Section 3: Querying Data with SELECT
### 1. Selecting All Columns
```sql
SELECT * FROM Students;
```
**Explanation**: Retrieves all columns from the Students table.

### 2. Selecting Specific Columns
```sql
SELECT FirstName, LastName, GPA FROM Students;
```
**Explanation**: Retrieves only the FirstName, LastName, and GPA columns.

### 3. Filtering with WHERE
```sql
SELECT * FROM Students
WHERE Major = 'Computer Science';
```
**Explanation**: Retrieves all students with a major in Computer Science.

### 4. Using Aggregate Functions
```sql
SELECT AVG(GPA) AS AverageGPA FROM Students;
```
**Explanation**: Calculates the average GPA of all students.

### 5. Grouping with GROUP BY
```sql
SELECT Major, COUNT(*) AS NumStudents
FROM Students
GROUP BY Major;
```
**Explanation**: Counts the number of students in each major.

### 6. Sorting with ORDER BY
```sql
SELECT FirstName, LastName, GPA
FROM Students
ORDER BY GPA DESC;
```
**Explanation**: Retrieves students sorted by GPA in descending order.

## 📖 Section 4: Join Operations
Joins allow you to combine data from multiple tables based on a related column.

### Example with INNER JOIN
Suppose we have another table Courses:
```sql
CREATE TABLE Courses (
    CourseID INTEGER PRIMARY KEY,
    CourseName TEXT,
    Instructor TEXT
);

INSERT INTO Courses (CourseID, CourseName, Instructor)
VALUES (1, 'Database Systems', 'Dr. Kim'),
       (2, 'Statistics', 'Dr. Patel');
```
**Query to Join Students and Courses:**
```sql
SELECT Students.FirstName, Students.LastName, Courses.CourseName
FROM Students
INNER JOIN Courses ON Students.Major = Courses.CourseName;
```
**Explanation**: Joins Students with Courses to match students’ majors with course names.

### Example with LEFT JOIN
Suppose we also have a table Enrollments that lists which students are enrolled in specific courses:
```sql
CREATE TABLE Enrollments (
    StudentID INTEGER,
    CourseID INTEGER,
    Semester TEXT
);

INSERT INTO Enrollments (StudentID, CourseID, Semester)
VALUES (1, 1, 'Fall 2024'),
       (2, 1, 'Fall 2024'),
       (3, 2, 'Spring 2024');
```
**Query to Left Join Students and Enrollments:**
```sql
SELECT Students.FirstName, Students.LastName, Enrollments.CourseID, Enrollments.Semester
FROM Students
LEFT JOIN Enrollments ON Students.StudentID = Enrollments.StudentID;
```
**Explanation**: This query returns all students from the Students table along with their course CourseID and Semester from the Enrollments table. Using LEFT JOIN, students without any matching enrollment records will still appear, with NULL values for CourseID and Semester.

## ✏️ Section 5: Practice Exercises
Try out these queries to solidify your understanding:

1. Retrieve all students with a GPA above 3.7.
2. Count how many students are in each major.
3. Update the Major of a specific student.
4. Delete records of students with a GPA below 2.5.

## 🚀 Wrapping Up
### Summary:
SQL allows us to create, modify, and query data in databases. <br>
Commands like SELECT, INSERT, UPDATE, and DELETE enable powerful data operations. <br>
Practice with JOINs, filtering, and aggregation to become proficient in SQL!
### Further Reading
[SQLBolt](https://sqlbolt.com/) - Interactive SQL lessons. <br>
[Mode SQL Tutorial](https://mode.com/sql-tutorial/) - Free SQL tutorial with practice queries. <br>
Happy Coding! :)

*Feel free to reach out to our team with any questions or for more resources!*
