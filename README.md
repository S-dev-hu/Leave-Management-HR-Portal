# 🚀 Leave Management & HR Portal

A professional **enterprise-style Leave Management & Human Resources Portal** built with **Python Flask**, **SQLite/PostgreSQL**, **Bootstrap**, and **Authentication & Role-Based Access Control**.

This application enables organizations to streamline leave requests, approvals, employee management, and HR reporting through a modern web interface.

---

## 📌 Overview

Managing employee leave manually using spreadsheets or emails can be inefficient and error-prone. This system centralizes leave management by providing a secure platform where employees can submit leave requests and managers can review, approve, or reject them.

The application follows a role-based structure similar to real-world HR systems used in modern organizations.

---

## ✨ Features

### 👤 Employee Features

-  Secure Login & Logout 
-  Employee Dashboard 
-  Submit Leave Applications 
-  View Leave Status 
-  Leave Balance Tracking 
-  View Leave History 
-  Profile Management 
-  Change Password 

### 👨‍💼 Manager Features

-  Manager Dashboard 
-  View Team Leave Requests 
-  Approve Leave Requests 
-  Reject Leave Requests 
-  Add Comments to Requests 
-  Employee Leave Monitoring 

### 🏢 HR Administrator Features

-  Employee Management 
-  User Account Management 
-  Department Management 
-  Leave Policy Configuration 
-  Generate Reports 
-  Leave Analytics 
-  System Administration 

---

## 📸 Screenshots

### Login Page

 \<img width="900" alt="Login" src="docs/screenshots/login.png"> 

### Employee Dashboard

 \<img width="900" alt="Dashboard" src="docs/screenshots/dashboard.png"> 

### Leave Request Form

 \<img width="900" alt="Leave Request" src="docs/screenshots/leave-request.png"> 

### Manager Approval Panel

 \<img width="900" alt="Approval Panel" src="docs/screenshots/approval-panel.png"> 

### Reports Dashboard

 \<img width="900" alt="Reports" src="docs/screenshots/reports.png"> 

---

## 🏗️ System Architecture

```
```

```
+---------------------+
|     Web Browser     |
+----------+----------+
           |
           v
+---------------------+
|     Flask App       |
+----------+----------+
           |
  -------------------
  |        |        |
  v        v        v
Auth   Leave Mgmt  Reports
Module  Module     Module

           |
           v
+---------------------+
| SQLite/PostgreSQL   |
+---------------------+
```

---

## 🛠️ Technology Stack

### Backend

-  Python 3.11+ 
-  Flask 
-  Flask-SQLAlchemy 
-  Flask-Login 
-  Flask-WTF 

### Frontend

-  HTML5 
-  CSS3 
-  Bootstrap 5 
-  JavaScript 

### Database

-  SQLite (Development) 
-  PostgreSQL (Production) 

### Authentication

-  Flask-Login 
-  Password Hashing 
-  Session Management 
-  Role-Based Access Control (RBAC) 

---

## 📂 Project Structure

```
```

```
Leave-Management-HR-Portal/
│
├── app.py
├── config.py
├── requirements.txt
├── README.md
│
├── instance/
│   └── leave_management.db
│
├── models/
│   ├── user.py
│   ├── employee.py
│   ├── leave_request.py
│   └── department.py
│
├── routes/
│   ├── auth.py
│   ├── employee.py
│   ├── manager.py
│   ├── admin.py
│   └── reports.py
│
├── forms/
│   ├── login_form.py
│   ├── leave_form.py
│   └── employee_form.py
│
├── templates/
│   ├── base.html
│   ├── login.html
│   ├── dashboard.html
│   ├── leave_request.html
│   ├── approvals.html
│   └── reports.html
│
├── static/
│   ├── css/
│   │   └── style.css
│   ├── js/
│   │   └── app.js
│   └── images/
│
└── docs/
    ├── screenshots/
    └── architecture/
```

---

# ⚙️ Setup & Installation

## 1️⃣ Clone the Repository

```
```

```
git clone https://github.com/yourusername/Leave-Management-HR-Portal.git

cd Leave-Management-HR-Portal
```

---

## 2️⃣ Create Virtual Environment

### Windows

```
```

```
python -m venv venv

venv\Scripts\activate
```

### Linux / macOS

```
```

```
python3 -m venv venv

source venv/bin/activate
```

---

## 3️⃣ Install Dependencies

```
```

```
pip install -r requirements.txt
```

---

## 4️⃣ Create Environment Variables

Create a file called:

```
```

```
.env
```

Add:

```
```

```
SECRET_KEY=super-secret-key

DATABASE_URL=sqlite:///leave_management.db
```

For PostgreSQL:

```
```

```
DATABASE_URL=postgresql://username:password@localhost/hr_portal
```

---

## 5️⃣ Initialize Database

```
```

```
flask db init

flask db migrate

flask db upgrade
```

Or:

```
```

```
python create_db.py
```

---

## 6️⃣ Create Admin User

```
```

```
python create_admin.py
```

Example:

```
```

```
Username: admin
Email: admin@company.com
Password: admin123
```

---

## 7️⃣ Run Application

```
```

```
python app.py
```

or

```
```

```
flask run
```

Application URL:

```
```

```
http://127.0.0.1:5000
```

---

# 🔑 Demo Credentials

### HR Admin

```
```

```
Username: admin
Password: admin123
```

### Manager

```
```

```
Username: manager
Password: manager123
```

### Employee

```
```

```
Username: employee
Password: employee123
```

---

# 📊 Database Design

### Users Table

| FieldType      |         |
| -------------- | ------- |
| id             | Integer |
| username       | String  |
| email          | String  |
| password\_hash | String  |
| role           | String  |

### Employees Table

| FieldType      |         |
| -------------- | ------- |
| id             | Integer |
| first\_name    | String  |
| last\_name     | String  |
| department     | String  |
| leave\_balance | Integer |

### Leave Requests Table

| FieldType    |         |
| ------------ | ------- |
| id           | Integer |
| employee\_id | Integer |
| leave\_type  | String  |
| start\_date  | Date    |
| end\_date    | Date    |
| status       | String  |

---

# 📈 Reports

The system can generate:

-  Leave Usage Report 
-  Department Leave Report 
-  Employee Leave Summary 
-  Pending Approvals Report 
-  Monthly Leave Trends 
-  Annual Leave Statistics 

---

# 🔒 Security Features

-  Password Hashing 
-  Session Management 
-  Role-Based Access Control 
-  CSRF Protection 
-  Secure Authentication 
-  Input Validation 
-  SQL Injection Protection 

---

# 🚀 Future Enhancements

-  Email Notifications 
-  Multi-Level Approval Workflow 
-  Calendar Integration 
-  Payroll Integration 
-  Mobile Application 
-  Employee Self-Service Portal 
-  Leave Forecast Analytics 
-  PDF Report Generation 
-  Microsoft Teams Integration 

---

# 🧪 Testing

Run tests:

```
```

```
pytest
```

Run coverage:

```
```

```
pytest --cov=app
```

---

# 🤝 Contributing

1.  Fork the repository 
2.  Create a feature branch 

```
```

```
git checkout -b feature/new-feature
```

3.  Commit changes 

```
```

```
git commit -m "Add new feature"
```

4.  Push branch 

```
```

```
git push origin feature/new-feature
```

5.  Open Pull Request 

---

# 📄 License

This project is licensed under the MIT License.

---

# 👨‍💻 Author

**Sibusiso Maseko**

-  GitHub: `https://github.com/S-dev-hu` 
-  LinkedIn: `https://linkedin.com/in/sibusiso-maseko-a5a21aab`
