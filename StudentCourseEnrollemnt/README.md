# 🎓 Student Course Registration System

A simple web-based app built using **Node.js**, **Express.js**, and **MySQL** for managing students, courses, and enrollments.

---

## 🚀 Features

- Manage students and courses  
- Enroll students in courses  
- View enrollment details  
- RESTful API with MySQL backend  

---

## ⚙️ Setup

1. **Install dependencies**
   ```bash
   npm install
   ```

2. **Create MySQL DB**
   ```sql
   CREATE DATABASE registration;
   USE registration;

   CREATE TABLE students (
     student_id INT PRIMARY KEY,
     name VARCHAR(100),
     email VARCHAR(100)
   );

   CREATE TABLE courses (
     course_id INT PRIMARY KEY,
     name VARCHAR(100)
   );

   CREATE TABLE enrollments (
     student_id INT,
     course_id INT,
     PRIMARY KEY (student_id, course_id),
     FOREIGN KEY (student_id) REFERENCES students(student_id),
     FOREIGN KEY (course_id) REFERENCES courses(course_id)
   );
   ```

3. **Run**
   ```bash
   node app.js
   ```
   App runs at **http://localhost:3000**

---

## 🖼 Screenshots

| Page | Preview |
|------|----------|
| 🏠 **Home Page** | ![Home](./assets/Home.png) |
| 👩‍🎓 **Student Details** | ![StudentDetails](./assets/StudentDetails.png) |
| 📚 **Course Details** | ![CourseDetails](./assets/CourseDetails.png) |
| 🧾 **Enrollment Details** | ![EnrollmentDetails](./assets/EnrollmentDetails.png) |
| 🔍 **View Details** | ![ViewDetails](./assets/ViewDetails.png) |

---

## 📜 License

MIT License © 2025

