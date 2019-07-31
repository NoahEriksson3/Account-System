# Account-System
An account-system for websites to be able to have specialized users with securely stored passwords.

The system is coded in php and uses mysql and phpmyadmin to store the passwords and usernames. 
I am using xampp to have a apache and mysql server. 

Download xampp here: https://www.apachefriends.org/index.html

# Guide to get up and running with the Account System.

1. Download and install xampp.
2. Start Apache and MySQL and click on admin for both of them.
3. In the phpmyadmin admin site you need to create a new database on the side where it says New.
4. When that is done you need to select your database on the side and then click SQL on the top row. 
5. Then you will need to execute this string to create the appropriate tables needed for the accounts:
 CREATE TABLE users (
    id INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    username VARCHAR(50) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL,
    created_at DATETIME DEFAULT CURRENT_TIMESTAMP
);
And when you pasted or wrote in this text you need to click run and then the tables have been created.
6. We will need to open the config.php file and edit some stuff mainly the database name if you haven't messed around with password and username for MySQL. You will change this text define('DB_NAME', 'account info');, change out account info to your database name and then you are setup with MySQL.
7. And lastly to get this up and running we will need to copy our files into the apache server for it to recognize our files and to run them. Go to C:\xampp\htdocs\dashboard and copy the entire repository into that folder. And just for good measure delete index.html we don't need that right now. 
8. Then you will go to this URL if everything is setup and running: http://localhost/dashboard/register.php
