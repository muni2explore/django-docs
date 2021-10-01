```bash
sudo apt update
sudo apt upgrade
sudo apt install apache2
sudo systemctl apach2 status
sudo systemctl status apache2


sudo apt install libexpat1

sudo apt install apache2-utils ssl-cert libapache2-mod-wsgi
sudo systemctl restart apache2


sudo a2enconf mod-wsgi
sudo systemctl restart apache2

sudo apt install pipenv


mkdir /var/www/projects/ivm-v2

source venv/bin/activate
pip install -r requirements.txt

vim wsgi.py
```

```python
"""
exposes the WSGI callable as a module-level variable named ``application``.
For more information on this file, see
https://docs.djangoproject.com/en/1.9/howto/deployment/wsgi/
"""
import os
import sys

from django.core.wsgi import get_wsgi_application

sys.path.append('/var/www/projects/ivm-v2')
# adjust the Python version in the line below as needed
sys.path.append('/var/www/projects/ivm-v2/venv/lib/python3.8/site-packages')

os.environ.setdefault("DJANGO_SETTINGS_MODULE", "config.settings")

application = get_wsgi_application()
```

```
sudo apt-get install python3-venv
python3 -m venv venv

sudo apt remove  libapache2-mod-wsgi
sudo apt install libapache2-mod-wsgi-py3

sudo a2enmod headers
sudo systemctl restart apache2
````
