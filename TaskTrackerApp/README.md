# Task Tracker Application

A simple full-stack task tracking web application built using React (frontend) and Node.js + Express + MySQL (backend).

# Features

- Add, edit, and delete tasks  
- Fields: title, description, status, (Pending/Done), priority, due_date.
- Mark tasks as Pending / Done    
- CSV export and download directly from the browser   

# Setup Instructions
Backend setup: 
>cd backend
>npm install

Create a .env file inside /backend and paste the following and enter your MySQL passwprd:
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=yourpassword
DB_NAME=tasktracker
DB_PORT=3306
PORT=5000

Run the backend using
>npm start


Frontend setup:
>npm install -->
>npm start

# Database schema:
CREATE DATABASE tasktracker;

USE tasktracker;

CREATE TABLE tasks (
  id INT AUTO_INCREMENT PRIMARY KEY,
  title VARCHAR(255) NOT NULL,
  description TEXT,
  status ENUM('Pending','Done') DEFAULT 'Pending',
  priority ENUM('Low','Medium','High') DEFAULT 'Medium',
  due_date DATE,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
