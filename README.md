# Django_Docker
Docker image for creating a Django project with a Postgres db.

1. Clone files to a new repository.
2. Run `docker-compose run web django-admin.py startproject <<PROJECT_NAME>> .`
3. Modify settings.py as 
```  
DATABASES = {
     'default': {
         'ENGINE': 'django.db.backends.postgresql',
         'NAME': 'postgres',
         'USER': 'postgres',
         'HOST': 'db',
         'PORT': 5432,
     }
 } 
```
4. Run project `docker-compose run web django-admin.py startproject <<PROJECT_NAME>> .`
` 
