# Fast API Project Setup and Basic Workflow

This guide will walk you through the steps to set up a FastAPI project, create routes, and handle database operations using SQLAlchemy.


## Installation and Setup

1. Create a virtual environment (optional but recommended):

   ```bash
   python -m venv env_name
   env_name\Scripts\activate   # On Windows
   source env_name/bin/activate   # On macOS or Linux
   ```
2. Install FastAPI and Uvicorn (ASGI server):

   ```bash
   pip install fastapi uvicorn
   ```
3. Install Flask-SQLAlchemy and python-multipart (for handling form data):

   ```bash
   pip install Flask-SQLAlchemy python-multipart
   ```


## Running the Project

- To run the FastAPI project, execute the following command from the project root directory:

    ```
    uvicorn app:app --reload
    ```

- The `--reload` option enables auto-reloading during development.


## Project Files Overview
- **app.py**: This file contains the main FastAPI application with route definitions.

- **database.py**: Defines the database connection and creates the SQLAlchemy engine and session.

- **models.py**: Contains the SQLAlchemy model definitions for your application. Currently, the `Todo` model is defined with `id`, `title`, and `complete` fields.

- **templates/base.html**: This is a sample HTML template file. You can add more templates as needed for your application.

## Routes and Functionality

- Home Route - `GET /`
    - Shows the list of todos from the database.
    - Renders the data using the Jinja2 template engine.
- Add Todo Route - `POST /add`
    - Accepts form data with a title to create a new todo item.
    - Adds the new todo to the database.
- Update Todo Route - `GET /update/{todo_id}`
    - Toggles the completion status of a todo item by its ID.
    - Updates the database with the new completion status.
- Delete Todo Route - `GET /delete/{todo_id}`
    - Deletes a todo item by its ID from the database.


## Adding More Functionality
To extend the functionality of your FastAPI project, you can:

- Implement more routes and views in `app.py`.
- Add new models and database operations in `models.py`.
- Create additional templates in the `templates` folder.

## Note
This FastAPI project uses SQLite as the database by default. If you prefer using PostgreSQL or any other database, update the `SQLALCHEMY_DATABASE_URL` in `database.py` accordingly.

That's it! You've set up a FastAPI project with basic routes and database operations using SQLAlchemy. Happy coding!