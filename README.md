

# ✈️ Airlines Management System

A Java-based full-stack project to manage airline operations like booking, ticketing, scheduling, and passenger records.

## 🚀 Features

- User registration and login
- Flight search and real-time booking
- Online ticket generation and cancellation
- Admin panel for managing flights, users, and staff
- Staff dashboard for check-ins and flight status
- Payment simulation (demo mode)

## 🛠️ Tech Stack

**Frontend:**
- HTML5, CSS3, JavaScript
- Bootstrap
- JSP/Servlets (for Java-based UI)

**Backend:**
- Java (JDK 17)
- JDBC
- Servlets / Spring Boot (optional upgrade)
- Apache Tomcat (Server)

**Database:**
- MySQL

## 🧱 Database Schema (MySQL)

```sql
CREATE TABLE flights (
  flight_id INT PRIMARY KEY AUTO_INCREMENT,
  airline_name VARCHAR(50),
  source VARCHAR(50),
  destination VARCHAR(50),
  departure_time DATETIME,
  arrival_time DATETIME,
  seat_capacity INT
);

CREATE TABLE users (
  user_id INT PRIMARY KEY AUTO_INCREMENT,
  username VARCHAR(50),
  password VARCHAR(255),
  email VARCHAR(100),
  role ENUM('admin', 'staff', 'passenger')
);

CREATE TABLE bookings (
  booking_id INT PRIMARY KEY AUTO_INCREMENT,
  user_id INT,
  flight_id INT,
  seat_number INT,
  booking_date DATETIME,
  FOREIGN KEY (user_id) REFERENCES users(user_id),
  FOREIGN KEY (flight_id) REFERENCES flights(flight_id)
);

📁 Project Structure

/AirlinesManagementSystem
├── /src
│   ├── /model
│   ├── /controller
│   ├── /view
│   └── /utils
├── /webapp
│   ├── index.jsp
│   ├── login.jsp
│   ├── adminDashboard.jsp
│   └── booking.jsp
├── /sql
│   └── schema.sql
├── README.md
└── pom.xml / build.gradle

👨‍💻 How to Run

1. Clone the repo:

git clone https://github.com/yourusername/airlines-management-system.git


2. Import into your IDE (Eclipse/IntelliJ).


3. Set up MySQL and import schema.sql.


4. Configure DBConnection.java with your database credentials.


5. Run on Apache Tomcat.



📸 Screenshots

Add screenshots of login page, booking system, admin panel, etc.

📜 License

This project is licensed under the MIT License.

🙌 Contributions

Feel free to fork and contribute. Pull requests are welcome!


---

> Developed as a student project for academic and learning purposes.

