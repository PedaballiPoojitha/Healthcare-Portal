# 🏥 Healthcare and Telemedicine Portal

## 📌 Project Overview

The **Healthcare and Telemedicine Portal** is a web-based healthcare management system designed to connect **patients and doctors** through a digital platform. It allows patients to book doctor appointments, consult with doctors online, and receive digital prescriptions.

The system provides separate dashboards for patients and doctors, making it easier to manage appointments, consultations, and prescriptions in an organized and efficient way.

This project was developed as part of **Java Full Stack Development Training** using technologies such as **Java, Spring Boot, HTML, CSS, JavaScript, MySQL, Hibernate/JPA, and REST APIs**.

---

## 🎯 Objectives

The main objectives of this project are:

* To provide an online platform for patients and doctors.
* To simplify the doctor appointment booking process.
* To allow doctors to manage patient appointments.
* To provide online consultation facilities.
* To enable doctors to create and provide digital prescriptions.
* To maintain healthcare-related information digitally.
* To reduce the need for physical visits for basic consultations.
* To provide a simple and user-friendly healthcare interface.

---

## ✨ Features

### 👤 Patient Module

* Patient registration and login
* Patient dashboard
* View available doctors
* Book doctor appointments
* Select appointment date and time
* Provide consultation reason
* View appointment status
* Online doctor consultation
* View digital prescriptions

### 👨‍⚕️ Doctor Module

* Doctor registration and login
* Doctor dashboard
* View patient appointments
* Approve appointments
* Complete consultations
* View patient details
* Provide diagnosis
* Add medicines and dosage
* Add consultation notes
* Generate digital prescriptions

### 📅 Appointment Management

The system supports the complete appointment workflow:

**Booked → Approved → Completed**

Doctors can approve or complete appointments, while patients can track their appointment status.

### 💊 Digital Prescription

Doctors can generate digital prescriptions containing:

* Diagnosis
* Medicines
* Dosage
* Notes
* Appointment information

Patients can view their prescriptions through the portal.

### 💬 Online Consultation

The portal is designed to support remote healthcare services, including online communication between patients and doctors through **chat and video consultation functionality**.

---

## 🛠️ Technologies Used

### Frontend

* HTML5
* CSS3
* JavaScript

### Backend

* Java
* Spring Boot
* Spring MVC
* REST APIs

### Database

* MySQL

### ORM

* Hibernate
* JPA

### Development Tools

* IntelliJ IDEA
* Maven
* MySQL Workbench
* Git & GitHub
* Postman

---

## 🏗️ Project Architecture

The application follows a layered architecture:

```text
Healthcare-Telemedicine-Portal
│
├── Frontend
│   ├── login.html
│   ├── patient-dashboard.html
│   ├── doctor-dashboard.html
│   ├── appointment.html
│   ├── book-appointment.html
│   └── prescription.html
│
├── Backend
│   └── Spring Boot Application
│       ├── Controller
│       ├── Service
│       ├── ServiceImpl
│       ├── Repository
│       └── Entity
│
└── Database
    └── MySQL
```

---

## 🔄 Application Workflow

```text
Patient
   │
   ├── Register / Login
   │
   ├── View Doctors
   │
   ├── Book Appointment
   │
   ▼
Appointment
   │
   ├── Booked
   ├── Approved
   └── Completed
   │
   ▼
Doctor Consultation
   │
   ├── Diagnosis
   ├── Medicines
   ├── Dosage
   └── Notes
   │
   ▼
Digital Prescription
   │
   ▼
Patient Views Prescription
```

---

## 🔌 REST API Endpoints

### Patient APIs

| Method | Endpoint              | Description       |
| ------ | --------------------- | ----------------- |
| POST   | `/api/patients`       | Register patient  |
| GET    | `/api/patients`       | Get all patients  |
| GET    | `/api/patients/{id}`  | Get patient by ID |
| PUT    | `/api/patients/{id}`  | Update patient    |
| DELETE | `/api/patients/{id}`  | Delete patient    |
| POST   | `/api/patients/login` | Patient login     |

### Appointment APIs

| Method | Endpoint                                | Description              |
| ------ | --------------------------------------- | ------------------------ |
| POST   | `/api/appointments`                     | Create appointment       |
| GET    | `/api/appointments`                     | Get all appointments     |
| GET    | `/api/appointments/{id}`                | Get appointment by ID    |
| PUT    | `/api/appointments/{id}`                | Update appointment       |
| DELETE | `/api/appointments/{id}`                | Delete appointment       |
| GET    | `/api/appointments/patient/{patientId}` | Get patient appointments |
| GET    | `/api/appointments/doctor/{doctorId}`   | Get doctor appointments  |

### Prescription APIs

| Method | Endpoint             | Description         |
| ------ | -------------------- | ------------------- |
| POST   | `/api/prescriptions` | Create prescription |
| GET    | `/api/prescriptions` | View prescriptions  |

---

## 🗄️ Database

The project uses **MySQL** for storing application data.

Main entities include:

* Patient
* Doctor
* Appointment
* Prescription

The relationships between these entities help manage appointments, consultations, and prescriptions efficiently.

---

## ⚙️ Installation and Setup

### 1. Clone the Repository

```bash
git clone <your-github-repository-url>
```

### 2. Open the Project

Open the project in **IntelliJ IDEA** or another Java IDE.

### 3. Configure MySQL

Create a database in MySQL:

```sql
CREATE DATABASE healthcare_portal;
```

Update the database configuration in:

```text
src/main/resources/application.properties
```

Example:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/healthcare_portal
spring.datasource.username=root
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

### 4. Build the Project

Using Maven:

```bash
mvn clean install
```

### 5. Run the Application

Run the Spring Boot main application class.

The backend will normally be available at:

```text
http://localhost:8080
```

---

## 🖥️ User Roles

### Patient

Patients can:

1. Register/Login
2. View doctors
3. Book appointments
4. Track appointments
5. Attend online consultations
6. View prescriptions

### Doctor

Doctors can:

1. Login
2. View appointments
3. Approve appointments
4. Complete consultations
5. Add diagnosis and medicines
6. Generate digital prescriptions

---

## 🔐 Security Considerations

The application is designed with separate patient and doctor workflows. In a production environment, additional security mechanisms can be implemented, such as:

* Password encryption
* JWT-based authentication
* Role-based authorization
* Secure API endpoints
* HTTPS
* Input validation
* Protection of patient medical information

---

## 🚀 Future Enhancements

The project can be further enhanced by adding:

* 🔐 JWT Authentication
* 👥 Role-based access control
* 💳 Online payment integration
* 📹 Real-time video consultation
* 💬 Real-time doctor-patient chat
* 📧 Email notifications
* 📱 Mobile application
* 🔔 Appointment reminders
* 📄 Downloadable PDF prescriptions
* 🩺 Electronic medical records
* ☁️ Cloud deployment
* 🔒 Advanced healthcare data security

---

## 📸 Project Screenshots

Add screenshots of the main pages here:

```text
Login Page
Patient Dashboard
Doctor Dashboard
Book Appointment
Appointment Management
Prescription Page
```

Example:

```markdown
![Login Page](screenshots/login.png)
![Patient Dashboard](screenshots/patient-dashboard.png)
![Doctor Dashboard](screenshots/doctor-dashboard.png)
![Appointment Page](screenshots/appointment.png)
![Prescription Page](screenshots/prescription.png)
```

---

## 👩‍💻 Developer

**P. Poojitha**

B.Tech – Computer Science and Technology
Madanapalle Institute of Technology and Science

### Technical Skills

* Java
* Spring Boot
* HTML
* CSS
* JavaScript
* MySQL
* Hibernate/JPA
* REST APIs
* Git & GitHub

---

## 📄 License

This project was developed for **academic and learning purposes** as part of Java Full Stack Development training.

---

## ⭐ Acknowledgement

I would like to thank my mentors and trainers for their guidance and support throughout the development of this project.

If you find this project useful, please consider giving it a ⭐ on GitHub.
