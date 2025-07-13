Student Management System (Java + PostgreSQL)
This is a console-based Java application that allows users to manage student records using
PostgreSQL. It supports creating, reading, updating, and deleting (CRUD) student data using
JDBC.

Features  
• Add new student records
• View all students
• Search student by ID
• Update existing student information
• Delete a student by ID
• Input validation for marks, email, and phone number  
Project Structure
student-management-system/  
├── main/  
  │ ├── java/  
  │ │ ├── App.java  
  │ │ ├── menu/  
  │ │ │ └── Menu.java  
  │ │ ├── DBoprations/  
  │ │ │ └── oprations.java  
  │ │ ├── database/  
  │ │ │ └── DBConnection.java  
  │ │ └── model/  
  │ │ └── Student.java  
Database Setup
1. Install and run PostgreSQL.  
2. Create a database named 'st'.  
3. Use the following SQL to create the table:  
CREATE TABLE students (  
id SERIAL PRIMARY KEY,  
name VARCHAR(100) NOT NULL,  
course VARCHAR(100) NOT NULL,  
marks INT CHECK (marks BETWEEN 0 AND 100),  
email VARCHAR(100),  
phone VARCHAR(15)  
);      
4. Update connection details in DBConnection.java if needed:  
private static final String URL = "jdbc:postgresql://localhost:5432/st";  
private static final String USER = "postgres";  
private static final String PASSWORD = "1895";    
System Requirements  
• Java 8 or higher  
• PostgreSQL  
• PostgreSQL JDBC driver  
Menu Options    
Outpu:-    
===== Student Management System =====  
   Add Student  
   View All Students  
   Search Student by ID  
   Update Student  
   Delete Student  
   Exit    
Input Validation Rules  
• Name and course cannot be empty    
• Marks must be between 0 and 100  
• Email must follow standard email format  
• Phone number must be exactly 10 digits  
Authors:-  
1.Vivek Keshav Havale  
2.Aniket Madanlal Sutar  
3.Viresh Siddharam Nimbargi  

