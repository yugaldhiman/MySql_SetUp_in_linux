# You can install MySQL on ubuntu

## 1: Update Package

- sudo apt update

## Step 2: Install MySQL Server

- sudo apt install mysql-server -y

## Step 3: Secure MySQL Installation

- sudo mysql_secure_installation

## Step 4: Verify MySQL Service

- sudo systemctl status mysql

## If it’s no running, start it with

- sudo systemctl start mysql

## Step 5: Access MySQL

- sudo mysql

## Create a database

- CREATE DATABASE database_name;

## Show databases

- SHOW DATABASES;

## Use a database

- USE database_name;

## Create a table

- CREATE TABLE table_name (
  id INT PRIMARY KEY AUTO_INCREMENT,
  name VARCHAR(100),
  age INT,
  email VARCHAR(100) UNIQUE
  );

## show tables

- SHOW TABLES;

## Rename a table

- RENAME TABLE old_table TO new_table;

## Insert a single row

- INSERT INTO table_name (name, age, email) VALUES ('John Doe', 25, 'john@example.com');

## Insert multiple rows

- INSERT INTO table_name (name, age, email) VALUES
  ('Alice', 22, 'alice@example.com'),
  ('Bob', 30, 'bob@example.com');

## Select show all records

- SELECT \* FROM table_name;

## Select specific columns

- SELECT name, email FROM table_name;

## Delete a specific record in table

- DELETE FROM table_name WHERE name = 'John Doe';

## Delete a table

- DELETE FROM table_name;

## Show current users

- SELECT user, host FROM mysql.user;

## Create a new user

- CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'password';

## Backup a database (command-line)

- mysqldump -u root -p database_name > backup.sql

## Restore a database (command-line)

- mysql -u root -p database_name < backup.sql
