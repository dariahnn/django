### To create a django project
django-admin startproject <nameoftheapplication>

### how to run a django project
python3 manage.py runserver

### DJANGO PROJECT FILES
1. manage.py :: command line utility allowing us to access the django project : entry file
2. todolist/ : this directory is the actual python project
3. __init__.py : this is an empty file that indicates above directory is a python project
4. asgi.py : this is an entry file fo ASGI compatible web servers to serve your project
5. wsgi.py : this is an entry file fo ASGI compatible web servers to serve your project
6. settings.py : settings/configuration file for the django project
7. urls.py : this are url declarations that map to our django app.


### HOW TO CREATE AN APP INSIDE A DJANGO PROJECT
python manage.py startapp <nameoftheapp>

### REGISTER THE APP
- GO to settings.py 

### DJANGO APP FILES
1. migrations/ : data migration files (empty initially)
2. __init__.py : indicates the app is a python application
3. admin.py : used to register models for the django admin panel
4. apps.py : contains the app configurations
5. models.py : defines the database models (tables)
6. tests.py : contains test cases of the app
7. views.py : this is the file to handle request-response logic (functional/controller)
8. urls.py (manually created on app level) : define url patterns for the app


### JINJA TEMPLATING
This is a syntax used to create django interfaces 
- To create templates
a. Inside the app folder create a template folder
b. Inside the templates you can create .html files, .css , .js
c. To consolidate the templating for our project , modify the following
- set a global templates directory for referencing our templates i.e.
 move the todolist templates folder to the global perspective
 i.e. root directory level
- register this change in settings.py for the project under the templates directory settings
        'DIRS' : [BASE_DIR / 'templates'], # Add this line

