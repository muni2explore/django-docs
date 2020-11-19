# Introduction

Django is Python framework to create web applications.

![Django](https://1.bp.blogspot.com/-06TQzLsy5Q4/X4R7-uFBYCI/AAAAAAAAMgo/nDbDD3S_GYcUuGCDCbpDuw7ytNY0FWTYACNcBGAsYHQ/s678/Screen%2BShot%2B2020-10-12%2Bat%2B9.23.13%2BPM.png)

## Create Project

### Step 1: Create new virtual environment and install dependencies using pipenv

```bash
PIPENV_IGNORE_VIRTUALENVS=1 pipenv install django~=3.1.2 --three
```

Where 
 - *PIPENV_IGNORE_VIRTUALENVS=1* - helps us to create new virtual environment and ignores already exisiting virtual environment
 - *--three* Python version 3
  
### Step 2: Start Virtual Environment

```bash
pipenv shell
```

### Step 3: Create new Django project 

```bash
django-admin startproject config .
```

### Step 4: Django Project folder structure:

```
.
├── Pipfile
├── Pipfile.lock
├── config
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
└── manage.py

1 directory, 8 files
```

 File        | Description
 --- | ---
 manage.py      | Run Django commands  
 \_\_init\_\_.py     | tells the python that folder contains the Python code
 wsgi.py & asgi.py | Webhooks for Apache/Nginx server
 settings.py | Configuration for Django project
 urls.py | Routes web request based on the URL pattern

### Step 5: Start Django Bulitin Server

```bash
python manage.py runserver
```
By default developement server starts on port 8000. If we want use different PORT than default one pass it as command-line argument.
```bash
python manage.py runserver 8080
```
If you want to change the server’s IP, pass it along with the port. For example, to listen on all available public IPs.
```bash
python manage.py runserver 0:8000
```
0 is a shortcut for 0.0.0.0

### Step 6: Create Django App

To create your app, make sure you’re in the same directory as manage.py and type this command:
```bash
python manage.py startapp APP_NAME
```

![Create new Django project using Pipenv](https://1.bp.blogspot.com/-w73fOcZpqFQ/X4RiauA8ZwI/AAAAAAAAMgc/7xUPyKvtAZ4R3oy1TcSP7S99xhIf149OQCNcBGAsYHQ/s2048/Screen%2BShot%2B2020-10-12%2Bat%2B7.34.06%2BPM.png)


![MVC FLow](https://1.bp.blogspot.com/-RVL0JuB2HpM/X4ReJvZIgAI/AAAAAAAAMgQ/kKHt7Fk_ooQfCAWU8utDWSqCzJRVwLwKgCNcBGAsYHQ/s795/Screen%2BShot%2B2020-10-12%2Bat%2B7.15.18%2BPM.png)
