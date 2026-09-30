
---

# README 2 — TFA 2: From Arrays to a Real Database

Copy everything below into the **second activity's `README.md`**:

```markdown
# POS System — From Arrays to a Real Database

A database-backed Point of Sale (POS) web application developed using **CodeIgniter 4**, **PHP**, and **MySQL**. This project extends the previous POS application by replacing static PHP arrays with a real MySQL database.

## Activity

**IT0049 – Web System Technologies**  
**Technical Formative Assessment 2**  
**From Arrays to a Real Database**

## Project Overview

The previous POS application stored customer and user information using static PHP arrays. In this activity, the application was updated to use a real MySQL database.

The system uses CodeIgniter 4 Models and Query Builder to retrieve customer and user records from the database and display them through the application's Views.

## Features

- MySQL database integration
- Customer Accounts page
- User Accounts page
- Database-backed customer records
- Database-backed user records
- CustomerModel
- UserModel
- Query Builder for retrieving records
- MVC architecture
- Organized Controllers, Models, and Views
- Database export included in the project

## Pages

| Page | URL | Description |
|------|-----|-------------|
| Home | `/` | Displays the POS system homepage |
| About | `/about` | Displays information about the application |
| Customer Accounts | `/customers` | Displays customer records retrieved from MySQL |
| User Accounts | `/users` | Displays user records retrieved from MySQL |

## Technologies Used

- PHP 8.2
- CodeIgniter 4.7.4
- MySQL
- HTML5
- CSS3
- XAMPP
- phpMyAdmin

## Database

The project uses a MySQL database named:

```text
pos_system

The database contains two tables:

Customers Table

The customers table stores customer account information.

Field	Type	Description
id	INT	Primary key
full_name	VARCHAR(100)	Customer's full name
email	VARCHAR(100)	Customer's email
phone	VARCHAR(20)	Customer's phone number
created_at	DATETIME	Date and time the record was created
Users Table

The users table stores user account information.

Field	Type	Description
id	INT	Primary key
username	VARCHAR(50)	Unique username
full_name	VARCHAR(100)	User's full name
created_at	DATETIME	Date and time the record was created

Each table contains at least five sample records as required by the activity.

CodeIgniter Models

The application uses separate Models for database access.

CustomerModel

The CustomerModel connects to the customers table and retrieves customer records using CodeIgniter's Query Builder.

UserModel

The UserModel connects to the users table and retrieves user records using CodeIgniter's Query Builder.

Database Retrieval

The Customer Accounts and User Accounts Controllers retrieve their records through their respective Models.

Example:

$customerModel = new CustomerModel();

$data = [
    'customers' => $customerModel->findAll()
];

The retrieved records are then passed to the corresponding Views for display.

Project Structure
POS System/
├── app/
│   ├── Controllers/
│   │   ├── Customers.php
│   │   ├── Users.php
│   │   └── Pages.php
│   │
│   ├── Models/
│   │   ├── CustomerModel.php
│   │   └── UserModel.php
│   │
│   └── Views/
│       ├── customers/
│       ├── users/
│       └── pages/
│
├── database/
│   └── pos_system.sql
│
├── public/
├── system/
├── vendor/
├── .env
├── composer.json
└── README.md
How to Run the Project Locally
1. Install XAMPP

Make sure Apache and MySQL are running through XAMPP.

2. Place the Project

Place the project folder inside:

C:\xampp\htdocs\training
3. Create the Database

Open phpMyAdmin and create a database named:

pos_system
4. Import the Database

Import the database export included in the project:

database/pos_system.sql
5. Configure the Database

Update the .env file with your local MySQL configuration:

database.default.hostname = localhost
database.default.database = pos_system
database.default.username = root
database.default.password =
database.default.DBDriver = MySQLi
database.default.port = 3306
6. Run the Application

Open the following URL in your browser:

http://localhost/training/
Database Export

The database export is included in the project:

database/pos_system.sql

This file contains the database structure and sample records for the customers and users tables.

Learning Objectives Demonstrated

This project demonstrates:

Configuring CodeIgniter database connections
Creating a MySQL database
Creating database tables
Creating CodeIgniter Models
Using Query Builder
Using findAll() to retrieve records
Passing database records from Controllers to Views
Separating application logic using MVC architecture
Replacing static PHP arrays with database records
Submission

The project includes:

GitHub repository containing the raw project files
Database export
Working CodeIgniter application
Hosted working version of the application

Developer:
Katrina Mangat
