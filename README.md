# Olympics24 Interactive Dashboard 

[![Awesome](https://awesome.re/badge.svg)](https://github.com/leelasaiprasanth/awesome-olympics-dashboard)
[![MIT License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Made with Python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)

<!-- ## Project Preview

![Olympics24 Dashboard](https://user-images.githubusercontent.com/105157723/200178020-a1a8d0c8-c1c0-4f3b-b0b8-f1e1f2c3e2f7.png) -->

## About

> This project aims to create an interactive dashboard for Olympic data visualization. The dashboard will be built using Django, PostgreSQL, and visualization libraries like Plotly, focusing on clean UI/UX and mobile responsiveness.

## Getting Started

### Prerequisites

* **Python** (3.8 or higher recommended)
* **Pip** (Python package installer)
* **PostgreSQL** (for dataset loading)

### Setup Instructions

1. **Clone the repository** to your local machine:

    ```bash
    git clone https://github.com/your_username/olympics24-dashboard.git
    cd olympics24-dashboard
    ```

2. **Create and activate a virtual environment**:
   
    On **Windows**:
    ```bash
    python -m venv venv
    venv\Scripts\activate
    ```

    On **macOS/Linux**:
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

3. **Install the dependencies**:
   
    ```bash
    pip install -r requirements.txt
    ```

4. **Create a `.env` file** for environment variables (e.g., database credentials). Use the `.env.example` as a template:

    ```bash
    cp .env.example .env
    ```

    Inside `.env`, define your environment variables:
    ```
    SECRET_KEY=your_secret_key
    DEBUG=True
    DATABASE_NAME=olympics24_db
    DATABASE_USER=your_db_user
    DATABASE_PASSWORD=your_db_password
    DATABASE_HOST=localhost
    DATABASE_PORT=5432
    ```

5. **Set up the PostgreSQL database**:

    Ensure you have PostgreSQL installed and running. Create a new database using the following command:
    ```bash
    createdb olympics24_db
    ```

6. **Run database migrations**:
   
    Apply Django migrations to set up the initial database structure.
    ```bash
    python manage.py migrate
    ```

7. **Load the dataset** into your PostgreSQL database (this step will vary depending on your dataset format). Example command if using CSV files:
   
    ```bash
    python manage.py loaddata path_to_your_data.csv
    ```

8. **Run the local development server**:
   
    ```bash
    python manage.py runserver
    ```

9. Open your browser and go to `http://127.0.0.1:8000/` to view the dashboard.

## Directory Structure

```bash
olympics24/
├── olympics24/          # Django project settings
├── paralympics24/       # Django app for dashboard
├── core/static/         # Static assets (CSS, JS, images)
├── core/templates/      # HTML templates for rendering views
├── core/datasets/       # Datasets for the dashboard
├── venv/                # Virtual environment folder
├── .env                 # Environment variables file
├── requirements.txt     # Dependencies file
└── manage.py            # Django management script
