# Database-Design-and-Creation

![1000_F_103537748_uWGohsy5YxltzX3xav3dQn9i23il3b7o](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/4226eef3-96e5-4c99-bb84-196672b5bb73)

## Table of Content
- [Project Overview](#Project-Overview)
- [Tools Used](#Tools-Used)
- [User Requirements](#User-Requirements)
- [Entities and Attributes](#Entities-and-Attributes)
- [Database Analyst User Requirement Interpretation](#Database-Analyst-User-Requirement-Interpretation)
- [Database ER Model Diagram](#Database-ER-Model-Diagram )
- [Creation of the Database](#Creation-of-the-Database)
- [Creation of the Database Entities Attributes and Values](#Creation-of-the-Database-Entities-Attributes-and-Values)
- [Coding SQL Statement to Generate reports](#Coding-SQL-Statement-to-Generate-reports)


### Project Overview
A new library has been built by a university, and a library database is needed to track the activities. The goal of this project is to design an entity relationship model for the proposed library database and create a database that stores and tracks data regarding books in the library, the authors of those books, the publishers of those books, and the students and employees who also borrow books from the library.

Note: All values are fictitious and were created with no organization in mind.

### Tools Used
- The DBMS used is MariaDB Server.
- The user interface used is HeidiSQL.
- I used Draw.io for the ER diagram model.

### User Requirements 
Requirement gathering process was conducted with the staff who worked in the library to determine their expectations from the database. 
The head of the library started by explaining the operating environment of the library as follows;
- There are multiple books authored by the same author in our collection.
- Authors may contribute to a single book or multiple books in our library.
- Some book publishers have multiple titles from their catalog featured in our library.
- Students have the option to borrow multiple books simultaneously, whereas employees are limited to borrowing one book at a time.
- Borrowing is restricted to one person per book, preventing group or team borrowings.

##### Major Reports Required:
###### Daily Reports:
- Closing staff must submit a daily report listing all borrowed books, including the names, IDs, and email addresses of the borrowers.
  
###### Monthly Stock Inventory:
- At the end of each month, a comprehensive stock inventory is conducted, encompassing all books in the library, whether currently borrowed or on the shelf.
  
###### Yearly Publisher Report:
- An annual report is compiled at the end of the academic year, providing information on all the publishers associated with the books in our library.

###### Shelf Organization:
- Our books are systematically arranged based on shelf location for ease of access and organization.

### Entities and Attributes 
##### BOOK
- Book ID
- Book Name
- No of Pages
- ISBN Number
##### AUTHOR
- Author ID
- Author Name
- Author Address
- Author Email 
##### PUBLISHER
- Publisher ID
- Publisher Name
- Publisher Address
- Publisher Email 
##### STUDENT
- Student ID
- Student Name
- Student Address
- Student Email
##### EMPLOYEE
- Employee ID
- Employee Name
- Employee Address
- Employee Email
##### SHELF
- Shelf ID
- Date Added
- Shelf Description (A to ZZ)

### Database Analyst User Requirement Interpretation
1. A book can be authored by many authors, and an author can write many books (Many-to-Many relationship).
2. A book is published by exactly one publisher, but a publisher can publish many books (Many-to-One relationship).
3. A student can borrow many books, and a book can be borrowed by exactly one student (One-to-Many relationship for students).
4. An employee can borrow at most one book, and a book can be borrowed by exactly one employee (One-to-One relationship for employees).
5. A book can at the most be on one shelf and at the least one shelf , a shelf can at the most have many books and at the least zero books. (one-to-many relationship).

### Database ER Model Diagram 
###### The construction of the database using Draw.io Workbench Model Editor
![LibraryDatabaseERDiagram2](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/a3730c7e-54b1-46a8-893e-829f1bfcee77)



### Creation of the Database

![1](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/5b69a932-a5b2-42b0-932c-f7f1c2ba5aac)


![2_](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/a20746bd-c43a-4718-84d1-0372cb9e899c)




### Creation of the Database Entities Attributes and Values
###### See raw sql codes used [here](LibraryDatabaseProjectSql_Codes.txt)

#### Student Table


![6](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/0d318259-b40b-4e06-9e50-3f55ac876942)


![7](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/0cf62cf2-e308-47e3-a678-4e6ae6b2dc3e)


![8](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/ca04dfea-003d-46da-afaa-2562ef6779e8)



#### Employee Table

![9](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/34a98bc5-456f-4663-9a27-2c26c2b50107)


![10](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/c7509892-1c1a-4003-91e8-05b6d25dc05e)


![11](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/f330905e-8e83-4710-918d-212beb42fb35)


#### Author Table
- [See]![12](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/029dea79-703e-47c6-a38c-5e3e99acdb46)
 create and insert query.
- [See]!![13](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/ba9e4762-5725-4d22-94de-80dced1b2612)
 entity and attributes.
- [See]![14](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/4a86b941-4fcc-4c68-8359-ba16f6b96c54)
 new records insert.

#### Publisher Table
- [See]![15](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/764e2119-24aa-428f-b852-7a18d3bd5415)
create and insert query.
- [See]![16](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/fc3a427c-bc1d-42c2-b4a3-bc329ebff983)
entity and attributes.
- [See]![17](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/cfc17c4e-4843-4ce1-86f4-1a55bba1a200)
 new records insert. 


#### Book Table
- [See]![18](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/19569219-e525-4175-8c59-564c030f2c74)
 create and insert query.
- [See]![19](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/cab1a950-182f-40e9-ab62-73ab5eea7143)
entity and attributes.
- [See] ![20](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/b82c18d8-0fc0-4296-89c9-a8efa1c3e963)
 new records insert.

#### Book_Auth Table
- [See]![21](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/5b7040e5-d506-48c6-b0aa-6050d49caee6)
 create and insert query.
- [See]![22](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/f85d9853-9285-4c0b-8a70-8b8c5d6b6538)
 entity and attributes.
- [See]![23](https://github.com/mtafviz/Database-Design-and-Creation/assets/134963936/bd6b4231-dae0-4874-9c95-4b972e4b41dd)
 new records insert.

### Coding SQL Statement to Generate reports
###### Closing staff must submit a daily report listing all borrowed books, including the names, IDs, and email addresses of the borrowers.
```SQL Statements
SELECT BookName, EmpName, EmpEmail, StuName, StuEmail,
FROM BOOK, EMPLOYEE, STUDENT,
WHERE EmpID.BOOK = EmpID.Employee
AND StuID.BOOK = StuID.Student;
```

###### At the end of each month, a comprehensive stock inventory is conducted, encompassing all books in the library, whether currently borrowed or on the shelf.
```SQL Statements
SELECT BookName, ISBNNUM,
FROM BOOK;
```

```SQL Statements
SELECT COUNT(BookID)
FROM BOOK;
```
