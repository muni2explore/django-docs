# MySQL & MariaDB

TO connect MySQL/MariaDB from Django install ``mysqlclient``

```bash
pipenv install mysqlclient
```

Then do the following changes in ``settings.py`` file.

```python
# https://docs.djangoproject.com/en/3.1/ref/settings/#databases
# https://docs.djangoproject.com/en/3.1/ref/databases/#mariadb-notes
DATABASES = {
    # 'default': {
    #     'ENGINE': 'django.db.backends.sqlite3',
    #     'NAME': BASE_DIR / 'db.sqlite3',
    # }
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'infosphere',
        'USER': 'muni',
        'PASSWORD': 'mysql',
        'HOST': '127.0.0.1',
        'PORT': '3306',
    }
}
```

## Keep MySQL Credentials in Conf file

### Step 1: Create my.cnf file in root directory

```
# my.cnf
[client]
database = infosphere
user = muni
password = mysql
default-character-set = utf8
host = 127.0.0.1
port = 3306
```

### Step 2: Update my.cnf file path in settings.py file

Import python default ``os`` module.

```python 
import os

....

'default': {
    'ENGINE': 'django.db.backends.mysql',
    'OPTIONS': {
        'read_default_file': os.path.join(BASE_DIR / 'my.cnf'),
    }
}
```




## Issues:

```
python manage.py migrate
Traceback (most recent call last):
  File "/Users/mayothi/.local/share/virtualenvs/infosphere--aDXd_wL/lib/python3.7/site-packages/django/db/backends/mysql/base.py", line 15, in <module>
    import MySQLdb as Database
ModuleNotFoundError: No module named 'MySQLdb'
```