# 🎓 Student Management System (Full Stack Project)

This is an in-class educational project designed to teach students how to build a full-stack application using **Java (Spring Boot)**, **Angular**, **MySQL**, and **Tailwind CSS**. The system supports **Admin**, **Teacher**, and **Student** roles with CRUD functionalities and optional JWT-based authentication.

---

## 🛠️ Tech Stack

| Layer       | Technology             |
|-------------|-------------------------|
| Frontend    | Angular, Tailwind CSS   |
| Backend     | Spring Boot, Java 17    |
| Database    | MySQL                   |
| ORM         | Hibernate (JPA)         |
| Build Tool  | Maven                   |
| Security    | Spring Security + JWT *(optional)*

---

## 🎯 Project Goals

- Teach layered backend architecture (Controller → Service → Repository).
- Build a responsive and interactive frontend.
- Learn how to work with MySQL and JPA for data persistence.
- Practice full-stack integration using RESTful APIs.
- Implement role-based access and optional authentication.

---

## 🧩 Features by Role

### 🔐 Admin
- Register, update, delete Students and Teachers.
- View all users.
- Admin dashboard.

### 👨‍🏫 Teacher
- Add, update, delete Courses.
- View Student profiles.
- Teacher dashboard.

### 👨‍🎓 Student
- View and update personal profile.
- Student dashboard.

---

## 🧱 Backend Folder Structure

src/
└── main/
├── java/
│ └── com.project.sms/
│ ├── controller/
│ ├── service/
│ ├── repository/
│ ├── entity/
│ ├── dto/
│ └── config/ # JWT/WebSecurity (optional)
└── resources/
├── application.properties
└── data.sql (optional for sample data)

pgsql
Copy
Edit

---

## 🌐 API Endpoints

### 🧑‍🎓 Student
- `POST /api/students` – Add new student (admin only)
- `GET /api/students` – Get all students
- `GET /api/students/{id}` – Get student by ID
- `PUT /api/students/{id}` – Update student
- `DELETE /api/students/{id}` – Delete student

### 👨‍🏫 Teacher
- `POST /api/teachers` – Add new teacher (admin only)
- `GET /api/teachers` – Get all teachers
- `GET /api/teachers/{id}` – Get teacher by ID
- `PUT /api/teachers/{id}` – Update teacher
- `DELETE /api/teachers/{id}` – Delete teacher

### 📘 Course
- `POST /api/courses` – Add course (teacher only)
- `GET /api/courses` – Get all courses
- `PUT /api/courses/{id}` – Update course
- `DELETE /api/courses/{id}` – Delete course

---

## 🔐 JWT Authentication *(Optional)*

- Token generation via login.
- Role-based access using `@PreAuthorize`.
- Store JWT token in frontend (Angular service).

---

## ⚙️ application.properties (Sample)

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/sms
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
server.port=8080
📋 Getting Started (Backend)
bash
Copy
Edit
# Clone the project
git clone https://github.com/your-username/student-management-system.git

# Import into IntelliJ or VS Code
# Set up MySQL Database
# Update application.properties
# Run the project
🧪 Testing
You can test endpoints via:

Postman or Insomnia

Swagger UI (if configured)

Angular frontend HTTP requests

📌 Notes for Students
Work through the project in phases: ER Design → Backend → Frontend → Integration → Security.

Use DTO classes for data transfer instead of exposing Entity classes directly.

Understand each layer’s responsibility in the architecture.

Optional: Try implementing JWT Authentication and secure routing.

📚 License
This project is developed for educational purposes only.
