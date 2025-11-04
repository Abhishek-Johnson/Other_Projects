# 🗒️ Task Tracker Application

A simple **full-stack task tracking app** built using **React (frontend)** and **Node.js + Express + MySQL (backend)**.

---

## 🚀 Features

- Add, edit, and delete tasks  
- Fields: title, description, status (Pending/Done), priority, due date  
- Toggle task status  
- Export tasks as CSV directly from the browser  

---

## ⚙️ Setup Instructions

### Backend

```bash
cd backend
npm install
```

Create a `.env` file in `/backend` and add:
```
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=yourpassword
DB_NAME=tasktracker
DB_PORT=3306
PORT=5000
```

Run the backend:
```bash
npm start
```

### Frontend

```bash
npm install
npm start
```

App runs at **http://localhost:3000**

---

## 🗄️ Database Schema

```sql
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
```

---

## 🖼 Screenshots

| Page | Preview |
|------|----------|
| 🏠 **Home Page** | ![Home](./assets/Home.png) |
| 📋 **Task List** | ![TaskList](./assets/TaskList.png) |

---

## 📜 License

MIT License © 2025
