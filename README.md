# Flask Scaffold

A simple Flask app creator that automatically generates a basic Flask project structure including models, routes, services, configuration, and more.

## Getting Started

This repository contains a utility script, [setup_flask_project.py](setup_flask_project.py), which creates a Flask project structure when executed.

## Prerequisites

- Python 3.7 or higher
- [Flask](https://flask.palletsprojects.com/)
- [Flask-SQLAlchemy](https://flask-sqlalchemy.palletsprojects.com/)
- [Flask-Migrate](https://flask-migrate.readthedocs.io/)
- [python-dotenv](https://pypi.org/project/python-dotenv/)

## Setup and Usage

1. **Clone the Repository**

   Clone this repository to your local machine.

2. **Run the Project Setup Script**

   From the root of the repository, run:

   ```sh
   python setup_flask_project.py
   ```

   This will create the following project structure:

   - **flask_app/**
     - **app/**
       - **models/**
         - `__init__.py`
         - `user.py`
         - `post.py`
       - **routes/**
         - `__init__.py`
         - `user_routes.py`
         - `post_routes.py`
       - **services/**
         - `__init__.py`
         - `user_service.py`
       - **config/**
         - `__init__.py`
         - `settings.py`
       - `extensions.py`
       - `__init__.py`
     - **migrations/**
     - `.env`
     - `config.py`
     - `requirements.txt`
     - `wsgi.py`
     - `run.py`

3. **Next Steps**

   After running the setup script, follow these steps:

   - Navigate into the generated project directory:

     ```sh
     cd flask_app
     ```

   - Create a virtual environment:

     ```sh
     python -m venv venv
     ```

   - Activate the virtual environment:

     - **Windows:** `venv\Scripts\activate`
     - **Mac/Linux:** `source venv/bin/activate`

   - Install dependencies:

     ```sh
     pip install -r requirements.txt
     ```

   - Initialize the database:

     ```sh
     flask db init && flask db migrate -m "Initial migration" && flask db upgrade
     ```

   - Run the app:

     ```sh
     python run.py
     ```

## Project Structure Overview

- **app/models**: Contains database models such as `User` and `Post` (user.py and post.py).
- **app/routes**: Defines routes using Blueprints for handling API endpoints (user_routes.py and post_routes.py).
- **app/services**: Holds service functions to manipulate or retrieve data (user_service.py).
- **app/config**: Stores configuration settings and environment-specific variables (settings.py).
- **app/extensions.py**: Initializes extensions like SQLAlchemy and Migrate.
- **app/**init**.py**: Creates and configures the Flask application.

## License

This project is licensed under the MIT License.

## Author

Nahom D  
Email: nahom@nahom.eu.org
