# Django-tutorial Screenshots & useful Commands
#### Django installed and running successfully
![Django](https://github.com/deesirouss/Django-tutorial/blob/main/mysite/installed%26runnig%20successfully.jpg "installed&runnig successfully")

#### Create app Polls and Browsed it
![Django](https://github.com/deesirouss/Django-tutorial/blob/main/mysite/created%20app%20polls%20running.jpg "created app polls and it is running")

#### All migrated tables in Postgresql database
![Django](https://github.com/deesirouss/Django-tutorial/blob/main/mysite/db-migrated%20tables.jpg "db-migrated tables")

#### Admin site Page looks like
![Django](https://github.com/deesirouss/Django-tutorial/blob/main/mysite/adminsite.jpg "admin site page")

### Useful commands
#### to check version of django:
> python -m django --version

#### to create project:
> django-admin startproject mysite

#### to create app:
> python manage.py startapp polls
 
#### to run server:
> python manage.py runserver

#### install required dependecies:
> sudo apt-get install libpq-dev python3-dev
> pip install psycopg2-binary

#### make some changes to your models, changes to be stored as a migration
> python manage.py makemigrations polls

#### The sqlmigrate command takes migration names and returns their SQL:
> python manage.py sqlmigrate polls 0001

#### this checks for any problems in your project without making migrations or touching the database:
> python manage.py check

#### remember the three-step guide to making model changes:

- Change your models (in models.py).
- Run python manage.py makemigrations to create migrations for those changes
- Run python manage.py migrate to apply those changes to the database.

#### to create a user who can login to admin site
> python manage.py createsuperuser

#### postgres commands to create user and db and grant privillages:
> CREATE DATABASE mydb;
> CREATE USER myuser WITH ENCRYPTED PASSWORD 'mypass';
> ALTER ROLE myuser SET client_encoding TO 'utf8';
> ALTER ROLE myuser SET default_transaction_isolation TO 'read committed';
> ALTER ROLE myuser SET timezone TO 'UTC';
> GRANT ALL PRIVILEGES ON DATABASE mydb TO myuser;
