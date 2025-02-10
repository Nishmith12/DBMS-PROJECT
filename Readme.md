# Department Activities and Resources Management System

![Sahyadri College Logo](https://via.placeholder.com/150x50?text=SCEM+Logo)  
*A project report submitted in partial fulfillment of the requirements for the DBMS Laboratory with Mini Project (V Sem B.E. CSE).*

---

## 📝 Description
This project aims to streamline the management of departmental activities (workshops, seminars, webinars, skill labs) and resources using a database-driven system. It provides an intuitive interface for administrators to perform CRUD operations, track enrollments, and manage event details efficiently. Built with **MySQL**, **PHP**, and a web-based interface, the system enhances coordination and resource utilization within academic departments.

---

## ✨ Features
- **CRUD Operations**: Create, Read, Update, and Delete records for workshops, seminars, coordinators, and resource persons.
- **Enrollment Management**: Track student enrollments for workshops and seminars.
- **Search & Sort**: Filter workshops by topic and sort by date.
- **Dashboard**: Overview of departmental activities and resources.
- **Normalized Database**: 3NF-compliant schema with relational integrity.

---

## 🛠 Technologies Used
- **Backend**: PHP, MySQL
- **Database Administration**: phpMyAdmin
- **Frontend**: HTML, CSS, JavaScript
- **IDE**: Visual Studio Code
- **Server**: XAMPP/WAMP/LAMP

---

## ⚙ Requirements
### Hardware
- Processor: 500 MHz or higher
- RAM: 4GB
- Storage: 500GB HDD

### Software
- MySQL Server
- PHP 7.0+
- Web Server (Apache/Nginx)
- Web Browser (Chrome/Firefox)

---

## 🚀 Installation
1. **Set Up a Local Server**  
   Install XAMPP/WAMP and start Apache + MySQL services.

2. **Create Database**  
   - Open phpMyAdmin and create a database named `college`.
   - Import the SQL tables using the schema from [Chapter 5](#chapter-5) of the report or run:
     ```sql
     CREATE TABLE department (
       dept_id VARCHAR(25) PRIMARY KEY,
       dept_name VARCHAR(25),
       dept_location VARCHAR(25)
     );
     -- Repeat for other tables (resource_person, workshop, student, etc.)
     ```

3. **Configure PHP Connection**  
   Update `connect.php` with your MySQL credentials:
   ```php
   <?php
   $HOSTNAME = 'localhost';
   $USERNAME = 'root';
   $PASSWORD = '';
   $DATABASE = 'college';
   $con = mysqli_connect($HOSTNAME, $USERNAME, $PASSWORD, $DATABASE);
   ?>