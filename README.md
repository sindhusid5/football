Developing a Node.js backend with a SQL database to facilitate CRUD operations for managing football players, including adding, editing, and deleting player records. 

1. Prerequestics:
   a.Node
   b.MySQL

2. Installing Dependencies
   git clone https://github.com/sindhusid5/football.git     //cloning the project
   cd football                                             //navigating to the project folder
   npm install                                            //installing the dependencies

3. Creating a Mysql Database 
    CREATE DATABASE ninja;
    CREATE TABLE IF NOT EXISTS players (
    ->   id int(5) NOT NULL AUTO_INCREMENT,
    ->   first_name varchar(255) NOT NULL,
    ->   last_name varchar(255) NOT NULL,
    ->   position varchar(255) NOT NULL,
    ->   number int(11) NOT NULL,
    ->   image varchar(255) NOT NULL,
    -> user_name varchar(20) NOT NULL,
    ->   ranking varchar(220) NOT NULL,
    ->   value decimal(10,2) NOT NULL,
    ->   PRIMARY KEY (id)
    -> ) ENGINE=InnoDB DEFAULT CHARSET=latin1 AUTO_INCREMENT=1;

4. Run the below commands on your workbench or MySQL command line to create a new client or user
   USE mysql;
   CREATE USER 'player'@'localhost' IDENTIFIED WITH mysql_native_password BY 'fOOtBa!!5';
   GRANT ALL PRIVILEGES ON . TO 'player'@'localhost';

5. Run the project
   node app.js

6. Open browser http://localhost:4200/
  
