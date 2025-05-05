# Smart City Management System

This project is a Smart City Management System built using **Python**, **Oracle Database**, **Flask**, **JavaScript**, and **HTML**. It provides a web interface for CRUD operations on multiple tables, allowing users to perform various database operations such as **search**, **insert**, **update**, and **delete**.

## Features

- **CRUD Operations**: Perform Create, Read, Update, and Delete actions on database tables.
- **Dynamic Forms**: Multiple HTML forms to handle each CRUD operation. 
  - **Search**: Search records based on conditions.
  - **Insert**: Insert new records into tables by selecting columns and providing values.
  - **Update**: Update existing records by selecting a column and entering a new value.
  - **Delete**: Delete records based on specified conditions.
- **Single Page Dashboard**: The homepage displays all tables and allows users to select a table and perform operations.
- **Custom SQL Statements**: Customize SQL queries by selecting columns, conditions, and values.

## Setup Instructions

Follow these steps to set up the project on your local machine:

### 1. **Open the Project in PyCharm**

   This project is designed for development in **PyCharm**. Open the project in PyCharm for an enhanced development experience.

### 2. **Configure the Database**

   - The system works with an **Oracle Database**. Make sure to have **Oracle Database** running and properly set up.
   - The required tables are initialized using the `smartcity_setup.sql` script. Execute this script in your Oracle database to set up the necessary tables.

### 3. **Install Required Libraries**

   This project relies on the following libraries:
   - **Flask**: Web framework for Python
   - **cx_Oracle**: Oracle database interface for Python
   
   Install them via **pip** by running:
   ```bash
   pip install Flask cx_Oracle
   ```
### 4. **Install Visual Studio C++**
cx_Oracle requires Visual Studio C++ version 14 or higher for installation. Make sure you have it installed. You can download it from the Visual Studio website.

### 5. **Update Database Configuration**
Before running the application, modify the database connection details in main.py as these are hardcoded in the script.

    Locate and update the following variables in main.py:

```bash
db_config = {
    "user": "your_db_username",        # Change this to your Oracle DB username
    "password": "your_db_password",    # Change this to your Oracle DB password
    "dsn": "localhost:1521/your_service_name"  # Change this to your Oracle DB DSN (Data Source Name)
}


# Tables to operate on
tables = ["Patients", "Students", "Education", "Hospital", "Traffic_Management", "Citizen", "Assets", "Transportation", "Property"]  # Update table names if needed
```

Ensure the table names and DB credentials match your local setup.

### 6. **Run the Application**
After the database configuration is updated, you can run the main application by executing:

```bash
python main.py
```
This will start the server, and you can access the Smart City Management System via your browser at:
```bash
http://localhost:5000
```

## Structure of the Application
- main.py: The main Python script that runs the application. It contains logic for handling CRUD operations and interactions with the database.

- templates/: Contains the HTML files for the web interface, including forms for CRUD operations.

- static/: Contains static files such as CSS and JavaScript to enhance the user interface.

- smartcity_setup.sql: SQL file to create the necessary tables in your Oracle database.

## Notes
- The application is built to manage a smart city system, allowing for CRUD operations on multiple tables such as Patients, Students, Traffic Management, and others. You can easily extend it to include additional tables if needed.

- Make sure to change the table names in main.py if you decide to modify or add new tables to the database.