# 🎫 Support Ticket Analyzer

A full-stack web application that enables customers to create support tickets and allows support teams to efficiently manage, track, and view customer issues.

Built using **Spring Boot**, **MySQL**, and **Vanilla JavaScript**, this project demonstrates RESTful API development with a clean separation between frontend and backend.

---

## 🚀 Features

- Create new support tickets
- View all submitted tickets
- View complete ticket details
- Automatic timestamp generation
- Default ticket status (`OPEN`)
- RESTful API architecture
- Responsive user interface

---

## 🛠 Tech Stack

### Frontend
- HTML5
- CSS3
- JavaScript

### Backend
- Java 17
- Spring Boot
- Spring Web
- Spring Data JPA

### Database
- MySQL

### Build Tool
- Maven

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

Before running the project, install:

- Java JDK 17+
- Maven
- MySQL Server
- Git
- VS Code or STS/IntelliJ IDEA
- Modern Web Browser

---

# 🗄️ Database Setup

Create a MySQL database.

```sql
CREATE DATABASE ticket_management_db;
```

Update the database credentials inside:

```text
Support_Ticket_Analyzer/src/main/resources/application.properties
```

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/ticket_management_db
spring.datasource.username=root
spring.datasource.password=YOUR_PASSWORD

spring.jpa.hibernate.ddl-auto=update
```

---

# ▶️ Running the Backend

Navigate to the backend folder.

```bash
cd Support_Ticket_Analyzer
```

Start the Spring Boot application.

```bash
mvn spring-boot:run
```

The backend will be available at:

```
http://localhost:8080
```

---

# ▶️ Running the Frontend

Navigate to the frontend folder.

```bash
cd Support_Ticket_Analyzer_Frontend
```

Open

```
index.html
```

using any web browser.

### Recommended

Use the **Live Server** extension in VS Code.

---

# 💻 How to Use

### 1. Create a Ticket

- Enter Customer Name
- Enter Issue Title
- Enter Issue Description
- Click **Submit**

---

### 2. View All Tickets

- Open the Dashboard
- All tickets will be fetched automatically from the backend.

---

### 3. View Ticket Details

- Click any ticket.
- View:
  - Customer Name
  - Issue Title
  - Issue Description
  - Status
  - Created Date & Time

---

# 📡 REST API

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | `/api/tickets` | Create Ticket |
| GET | `/api/tickets` | Get All Tickets |
| GET | `/api/tickets/{id}` | Get Ticket by ID |

---

## Sample Request

```json
POST /api/tickets

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
