# Django_Docker
Docker image for creating a Django project with a Postgres db.

1. Clone files to a new repository.
2. Run `docker-compose run web django-admin.py startproject <<PROJECT_NAME>> .`
3. Modify settings.py as 
` version: '2'
 services:
   db:
     image: postgres
   web:
     build: .
     command: python manage.py runserver 0.0.0.0:8000
     volumes:
       - .:/code
     ports:
       - "8000:8000"
     depends_on:
       - db`
4. Run project `docker-compose run web django-admin.py startproject <<PROJECT_NAME>> .`
` 
