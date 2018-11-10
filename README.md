# Django-rest-shop
A simple Django-rest-shop built with React and Django REST Framework(DRF).

## Dependencies
* Python3+
* Node
* PostgreSQL

## Getting Started
### Installation
Clone this repository:

    git clone https://github.com/yantadeu/django-rest-shop.git

Create virtualenv and install all requirements in **backend** directory:

    cd django-rest-shop/backend/
    python3 -m venv venv_name
    source venv_name/bin/activate
    pip install -r requirements.txt

Install all needed node_modules in **frontend** directory:

    cd django-rest-shop/frontend/
    yarn install

or with npm:

    npm install

Prepare database in postgreSQL:

    sudo -u postgres psql
    CREATE DATABASE django_rest_shop; # Don't forget the semicolon in the end

    # Quit postgresql shell
    \q

Set up database connection in **django-rest-shop/backend/backend/settings.py** in DATABASES section:

    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.postgresql_psycopg2',
            'NAME': 'django_rest_shop',
            'USER': 'YOUR_USERNAME', # replace with your own username
            'PASSWORD': 'YOUR_PASSWORD', # replace with your own password
            'HOST': 'localhost',
            'PORT': ''
        }
    }

Fire up **backend** server:

    cd django-rest-shop/backend/
    python manage.py migrate
    python manage.py runserver

Open another terminal for **frontend** server:

    cd django-rest-shop/frontend/
    yarn start

or with npm:

    npm start