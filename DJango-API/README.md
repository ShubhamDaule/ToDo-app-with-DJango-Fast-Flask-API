# Django API Project Setup and Basic Workflow

This guide will walk you through the steps to create a Django project, add views, templates, and models, and integrate them into the administration site.


## Installation and Setup

1. Create a virtual environment (optional but recommended):
   ```console
   python -m venv env_name
   env_name\Scripts\activate   # On Windows
   source env_name/bin/activate   # On macOS or Linux
   ```

2. Install Django:
    ```console
    pip install Django
    ```

3. Create a new Django project:
    ```console
    django-admin startproject project_name
    ```


## Starting the Development Server

1. Navigate to the project directory:
    ```console
    cd project_name
    ```

2. Start the development server:
    ```console
    python manage.py runserver
    ```

3. Create a new app within the project:
    ```console
    python manage.py startapp app_name

    ```

4. Add `app_name` to the `INSTALLED_APPS` list in `settings.py`:


## Adding Views and URLs

1. Implement views in `app_name.views.py` and create `app_name.urls.py`.

2. Register the app's URLs in the project's `urls.py`:

## Adding Templates

1. Create a `templates` folder in the app directory.

2. Add your HTML templates to the `templates` folder.

3. In `settings.py`, add the `templates` directory to the `DIRS` list:

4. Modify your views to use the `render` function to render the templates:


## Adding Models

1. Implement your models in `app_name.models.py`.

2. Create database tables and migrations:
    ```console
    python manage.py makemigrations
    python manage.py migrate
    ```

3. Create a superuser to access the admin site:
    ```console
    python manage.py createsuperuser
    ```

## Integrating Models with the Admin Site
1. Register your models in `app_name.admin.py`.

2. Access the admin site by running the development server and navigating to http://127.0.0.1:8000/admin/. Log in using the superuser credentials.

3. Add records to your models using the admin interface.

## Adding CSRF Token to Templates
- Add `{% csrf_token %}` to your HTML templates inside the `<form>` tags to protect against CSRF attacks.
