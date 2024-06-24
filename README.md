 
# Developing a Node.js Backend with MySQL for Football Player Management

This guide will help you set up a Node.js backend with a MySQL database to facilitate CRUD (Create, Read, Update, Delete) operations for managing football players.

## Prerequisites

Make sure you have the following installed on your machine:
- Node.js
- MySQL

## Steps

### 1. Installing Dependencies

1. **Clone the repository to your local machine:**

   ```bash
   git clone https://github.com/sindhusid5/football.git
   ```

2. **Navigate to the project directory:**

   ```bash
   cd football
   ```

3. **Install the necessary dependencies:**

   ```bash
   npm install
   ```

### 2. Setting Up the MySQL Database

1. **Create a MySQL Database:**

   Open your MySQL Workbench or MySQL command line and run the following commands:

   ```sql
   CREATE DATABASE ninja;
   USE ninja;
   CREATE TABLE IF NOT EXISTS players (
       id int(5) NOT NULL AUTO_INCREMENT,
       first_name varchar(255) NOT NULL,
       last_name varchar(255) NOT NULL,
       position varchar(255) NOT NULL,
       number int(11) NOT NULL,
       image varchar(255) NOT NULL,
       user_name varchar(20) NOT NULL,
       ranking varchar(220) NOT NULL,
       value decimal(10,2) NOT NULL,
       PRIMARY KEY (id)
   ) ENGINE=InnoDB DEFAULT CHARSET=latin1 AUTO_INCREMENT=1;
   ```

2. **Create a MySQL User:**

   Run the following commands to create a new user and grant privileges:

   ```sql
   USE mysql;
   CREATE USER 'player'@'localhost' IDENTIFIED WITH mysql_native_password BY 'fOOtBa!!5';
   GRANT ALL PRIVILEGES ON ninja.* TO 'player'@'localhost';
   ```

### 3. Running the Project

1. **Start the Node.js application:**

   ```bash
   node app.js
   ```

2. **Open your web browser and navigate to:**

   ```url
   http://localhost:4200/
   ```

### Additional Notes

- Ensure that your MySQL server is running before you start the Node.js application.
- If you encounter any issues with database connections, check your `app.js` file for the correct MySQL credentials and database name.
 
