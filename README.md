# 🎫 Support Ticket Analyzer

A full-stack web application that enables customers to create support tickets and allows support teams to efficiently manage, track, and view customer issues.

Built using **Spring Boot**, **MySQL**, and **Vanilla JavaScript**, this project demonstrates RESTful API development with a clean separation between frontend and backend.

---

## 🚀 Features

* Create new support tickets
* View all submitted tickets
* View complete ticket details
* Automatic timestamp generation
* Default ticket status (`OPEN`)
* RESTful API architecture
* Responsive user interface

---

## 🛠 Tech Stack

### Frontend

* HTML5
* CSS3
* JavaScript

### Backend

* Java 17
* Spring Boot
* Spring Web
* Spring Data JPA

### Database

* MySQL

### Build Tool

* Maven

---

## 📂 Project Structure

```text
Ticket_Analyzer/
│
├── Support_Ticket_Analyzer/
│   ├── src/
│   └── pom.xml
│
├── Support_Ticket_Analyzer_Frontend/
│   ├── index.html
│   ├── css/
│   ├── js/
│   └── assets/
│
└── README.md
```

---

# ⚙️ Prerequisites

Before running the project, install the following:

* Java JDK 17+
* Maven
* MySQL Server
* Git
* VS Code / STS / IntelliJ IDEA
* Modern Web Browser

---

# 📥 Clone the Repository

Clone the repository from GitHub.

```bash
git clone https://github.com/SasiVenkatGowdDasari/Ticket_Analyzer.git
```

Navigate into the project folder.

```bash
cd Ticket_Analyzer
```

You should now have the following folders:

```text
Support_Ticket_Analyzer/
Support_Ticket_Analyzer_Frontend/
```

---

# 🗄️ Database Setup

Create a MySQL database.

```sql
CREATE DATABASE ticket_management_db;
```

Open

```text
Support_Ticket_Analyzer/src/main/resources/application.properties
```

Update your database credentials.

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/ticket_management_db?useSSL=false&serverTimezone=UTC
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD

spring.jpa.hibernate.ddl-auto=update
```

The application will automatically create the required tables on startup.

---

# ▶️ Running the Backend

Open a terminal.

Navigate to the backend project.

```bash
cd Support_Ticket_Analyzer
```

Install dependencies and start the Spring Boot server.

```bash
mvn clean install
```

```bash
mvn spring-boot:run
```

Backend URL

```
http://localhost:8080
```

---

# ▶️ Running the Frontend

Open another terminal.

Navigate to the frontend folder.

```bash
cd Support_Ticket_Analyzer_Frontend
```

Open

```
index.html
```

in your browser.

### Recommended

Run the frontend using the **Live Server** extension in VS Code.

The frontend communicates with

```
http://localhost:8080
```

Ensure the backend is running before opening the frontend.

---

# 💻 How to Use

### Step 1 — Start the Backend

Run the Spring Boot application.

```
http://localhost:8080
```

---

### Step 2 — Open the Frontend

Open

```
index.html
```

using Live Server or any web browser.

---

### Step 3 — Create a Ticket

Fill in:

* Customer Name
* Issue Title
* Issue Description

Click **Submit**.

---

### Step 4 — View All Tickets

The dashboard automatically loads every ticket from the backend.

---

### Step 5 — View Ticket Details

Click any ticket to see:

* Customer Name
* Issue Title
* Issue Description
* Ticket Status
* Created Date & Time

---

# 📡 REST API

| Method | Endpoint            | Description      |
| ------ | ------------------- | ---------------- |
| POST   | `/api/tickets`      | Create Ticket    |
| GET    | `/api/tickets`      | Get All Tickets  |
| GET    | `/api/tickets/{id}` | Get Ticket by ID |

---

## Sample Request

```http
POST /api/tickets
```

```json
{
  "customerName": "John Doe",
  "issueTitle": "Login Issue",
  "issueDescription": "Unable to login."
}
```

---

## Sample Response

```json
{
  "id": 1,
  "customerName": "John Doe",
  "issueTitle": "Login Issue",
  "issueDescription": "Unable to login.",
  "status": "OPEN",
  "createdAt": "2026-06-25T10:30:00"
}
```

---

---

