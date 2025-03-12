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

### DATABASES
Organised collection of data that allows users to store, retrieve , update and delete information more effectively.
### TYPES OF DATABASES
1. Relational Databases
store data in tables : rows(records) and columns(fields)
tables can be related
uses the SQL query language
2. NoSQL Databases
3. In-Memory Databases
### WHY USE DB's 
1. Persistent data storage
2. Efficient data retrieval
3. Data relationship
4. Security an integrity
### USING DB's IN DJANGO
1. Define the model data
2. Use django migration commands to convert our models into actual database tables
3. Object Relational Mappers(ORM's ) to interact with the db using python code instead of raw SQL statements 
### TO CONVERT MODELS TO TABLES
1. python3 manage.py makemigrations appname
2. python3 manage.py migrate
### DATABASE CREATION
1. Double click on the db.sqlite
2. click the + sign or the prompt to create the data source(for development use sqlite)
### RELATIONAL DATABASES: DATABASE RELATIONSHIPS
1. One to Many relationship
- Taskers table (contain the users who perform the tasks)
- Task table(Contains the tasks)
To establish a one to many relationship establish a foreign key
- a unique key pointing to a unique reference in another db table 
2. Many to many relationship

### HOW TO ADD IMAGES (STATIC)
Django uses static directory
templates directory/ => static/ => images/
Add {%load static%} at the top of the html file
# Ensure Django knows where to find static 