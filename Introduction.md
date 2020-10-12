# Introduction

Django is Python framework to create web applications.

## Create Project

### step 1: Create new virtual environment and install dependencies using pipenv

```bash
PIPENV_IGNORE_VIRTUALENVS=1 pipenv install django~=3.1.2 --three
```

Where 
 - *PIPENV_IGNORE_VIRTUALENVS=1* - helps us to create new virtual environment and ignores already exisiting virtual environment
 - *--three* Python version 3
  
### step 2: Start Virtual Environment

```bash
pipenv shell
```

### step 3: Create new Django project 

```bash
django-admin startproject config .
```

### step 4: Django Project folder structure:

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

### step 5: Start Django Bulitin Server
```bash
python manage.py runserver
```

### Step 6: Create Django App
```bash
python manage.py startapp APP_NAME
```

![Create new Django project using Pipenv](https://1.bp.blogspot.com/-w73fOcZpqFQ/X4RiauA8ZwI/AAAAAAAAMgc/7xUPyKvtAZ4R3oy1TcSP7S99xhIf149OQCNcBGAsYHQ/s2048/Screen%2BShot%2B2020-10-12%2Bat%2B7.34.06%2BPM.png)


![MVC FLow](https://1.bp.blogspot.com/-RVL0JuB2HpM/X4ReJvZIgAI/AAAAAAAAMgQ/kKHt7Fk_ooQfCAWU8utDWSqCzJRVwLwKgCNcBGAsYHQ/s795/Screen%2BShot%2B2020-10-12%2Bat%2B7.15.18%2BPM.png)
