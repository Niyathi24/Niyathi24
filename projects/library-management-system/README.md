# Library Management System

## Problem Statement

Developing a web application from scratch for a library management system.

## Description

The requirement was to create a web application, Library Management System using Flask.

## Environment

**Hardware Specification:**
- Standard computer/laptop

**Software Specification:**
- Virtual environment: venv
- Framework: Flask
- Language: Python
- Frontend: HTML, CSS, JavaScript

## Application Features

### Book Management
- Adding a book
- Editing a book
- Deleting a book

### User Management
- Adding a user
- Editing a user
- Deleting a user

### System
- Login/User authentication

## Architecture
```
┌─────────────────┐
│ Database Server │
│    (SQLite3)    │
└────────┬────────┘
         │
┌────────▼────────┐      ┌──────────────────┐      ┌──────────┐
│   Web Server    │◄────►│ Application      │◄────►│  Client  │
│    (Flask)      │      │ Server (Flask)   │      │(Browser) │
└─────────────────┘      └──────────────────┘      └──────────┘
```

## Getting Started

### Prerequisites
- Python 3.x
- pip

### Installation

1. Clone the repository
```bash
git clone <repository-url>
cd library-management-system
```

2. Create a virtual environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies
```bash
pip install flask
```

4. Run the application
```bash
python app.py
```

## Technologies Used

- **Backend:** Flask (Python)
- **Frontend:** HTML, CSS, JavaScript
- **Database:** SQLite3
- **Environment:** Python Virtual Environment

## Features Implemented

- User authentication and login
- Book CRUD operations (Create, Read, Update, Delete)
- User CRUD operations
- Role-based access control
- Responsive UI design
- Database schema design with normalization

## Author

Sreeniyathi Kasireddy
