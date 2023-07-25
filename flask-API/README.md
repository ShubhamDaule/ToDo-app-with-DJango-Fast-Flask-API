# Flask API Project Setup and Basic Workflow

This is a simple To-Do app built with Flask and SQLAlchemy to manage your tasks.


## Setup and Installation

1. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv env_name
   env_name\Scripts\activate   # On Windows
   source env_name/bin/activate   # On macOS or Linux
   ```

2. Install required packages:
    ```
    pip install Flask Flask-SQLAlchemy
    ```


## Running the App

Before running the app, set the environment variables for Flask:

- Windows (CMD):
    ```
    set FLASK_APP=app.py
    set FLASK_ENV=development
    ```

- Windows (PowerShell):
    ```
    $env:FLASK_APP = "app.py"
    $env:FLASK_ENV = "development"
    ```

- macOS/Linux (Terminal):
    ```
    export FLASK_APP=app.py
    export FLASK_ENV=development
    ```


- Start the development server:
    ```
    flask run
    ```
    
The app will be accessible at http://127.0.0.1:5000.


### Database Configuration
The app uses SQLite as the database. The database configuration can be found in `app.py`. By default, it uses a SQLite database (`db.sqlite`).


### Models
The app uses the `Todo` model to represent a single to-do item with a title and a completion status. The model definition is in `app.py`.


### Templates
The `templates` folder contains the base HTML template (`base.html`) used by the app.


### Endpoints
- `GET /`: Displays the list of all to-do items.

- `POST /add`: Adds a new to-do item. It expects a form field title with the title of the new to-do.

- `GET /update/<int:todo_id>`: Toggles the completion status of a to-do item with the given todo_id.

- `GET /delete/<int:todo_id>`: Deletes the to-do item with the given todo_id.

That's it! You now have a basic To-Do app built with Flask and SQLAlchemy. Feel free to extend and customize it further to suit your needs.

