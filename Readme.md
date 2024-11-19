# Olympics24 Django Project

This project is a Django-based web application designed for processing and visualizing the Olympics24 dataset. It uses a modular architecture, environment variables for secure configuration, and PostgreSQL for database management.

---

## Features
- Modular app: `processdata` for handling data endpoints.
- Secure environment configuration using `.env` files.
- PostgreSQL database integration for scalability.
- Virtual environment setup for isolated development.
- Contributor guidelines for smooth collaboration.

---

## Prerequisites
Ensure the following are installed on your system:
1. **Python** (3.8 or later) - [Install Python](https://www.python.org/downloads/)
2. **PostgreSQL** (if applicable) - [Install PostgreSQL](https://www.postgresql.org/download/)
3. **Git** (for version control) - [Install Git](https://git-scm.com/downloads)

---

## Setup Instructions

### **1. Clone the Repository**
First, clone the repository to your local machine:
```bash
git clone https://github.com/<your-username>/olympics24.git
```

### **2. Create and Activate a Virtual Environment**
To create a virtual environment that isolates the project dependencies:
```bash
python -m venv venv
```

Windows:
```bash
.\venv\Scripts\Activate.ps1
```
Once activated, your terminal should show (venv) at the beginning of the prompt.

To deactivate the virtual environment, run:
```bash
deactivate
```
To Update the requirements.txt file, run:
```bash
pip freeze > requirements.txt
```

Running the Application
```bash
python manage.py makemigrations
```

To create a superuser, run:
```bash
python manage.py migrate
```