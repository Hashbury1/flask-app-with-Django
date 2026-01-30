Flask-Django Hybrid ApplicationThis repository contains a unique web application architecture that leverages the strengths of both Flask and Django. This hybrid approach allows for a lightweight, flexible frontend or API (Flask) while utilizing the robust "batteries-included" features of Django (Admin panel, ORM, and Authentication).🚀 

Project Overview

In this setup:Flask acts as the [e.g., lightweight API gateway or microservice] handling [specific task].

Django provides the [e.g., backend management system, database migrations, and administrative interface].🏗️ 

Architecture DesignFeatureHandled ByWhy?User InterfaceFlaskRapid prototyping and minimal overhead for specific routes.

Admin DashboardDjangoLeverages the built-in django-admin for data management.Database/ORM

Django

Uses Django Models for easy migrations and complex queries.API Endpoints

Flask/DjangoHybrid routing for performance and scalability.🛠️ Getting Started

Prerequisites

Python 3.9 or higherpip (Python package manager)Virtual environment (recommended)

Installation

Clone the Repository:Bashgit clone https://github.com/Hashbury1/flask-app-with-Django.git
cd flask-app-with-Django

Set Up a Virtual Environment:Bashpython -m venv venv

source venv/bin/activate  # On Windows: venv\Scripts\activate

Install Dependencies:Bashpip install -r requirements.txt

Database Setup (Django):Bashpython manage.py makemigrations

python manage.py migrate

python manage.py createsuperuser # To access the Django Admin
🏃 Running the Application

Because this is a hybrid app, you may need to run two separate development servers or a unified WSGI wrapper.Option 1: Running Separately

To start the Django Backend:Bashpython manage.py runserver 8000

To start the Flask Frontend:Bashexport FLASK_APP=app.py
flask run --port 5000

Option 2: Unified WSGI (If configured)

If the project uses DispatcherMiddleware to combine the apps:Bashpython run_combined.py
📁 Repository Structure


🧪 TestingTo run tests for both frameworks:Bash# Django tests
python manage.py test

# Flask tests (using pytest)
pytest flask_frontend/tests.py
🤝 ContributingContributions are welcome! If you'd like to improve the integration between the two frameworks or add new features:Fork the Project.Create your Feature Branch (git checkout -b feature/AmazingFeature).Commit your Changes (git commit -m 'Add some AmazingFeature').Push to the Branch (git push origin feature/AmazingFeature).Open a Pull Request.
