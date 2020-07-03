---
marp: true

---

# Django Tutorial

---

# Installing Django
To install django we can type in the command line:
```
pip3 install django
```
or if we already have django we can just upgrade to the specified version by:
```
pip3 install --upgrade django==3.0
```

---
## Starting a project
Let's say we want to make a todo app. On a specified folder, e.g. project_django folder, you can type: 

```
python3 manage.py startproject todo
```

---
# Project file structure
By default the project files will be structured like:
> project_django/
> > manage.py
> > todo/
> > > settings.py
> > > urls.py
> > > asgi.py
> > > wsgi.py

---

## Run development server
To check if the project is successfully created, on the same folder of manage.py run the development server:
> project_django/
```
python3 manage.py runserver
```
access the web page by the indicated location, e.g.
> localhost:8000

To stop the server we can use `Ctrl+c`

---

## Migrate the database
By default, django has included some database when we created the project, e.g. user database, to activate the database we have to migrate it into our project by doing:

```
python3 manage.py makemigrations
```
and
```
python3 manage.py migrate
```
---

## Create superuser for the app
After the user databse is activated we can create superuser for the app:
```
python3 manage.py createsuperuser
```
We will be prompted to fill the username, email, and password.

<br><br><br>
_Note that the password will not be shown on the screen_

---

## Let's check the admin page
By default django also include simple admin page that powerful enough for our needs
> localhost:8000/admin

To access the admin page, we can input the user we just created.

---

## Starting new app
Django use a modular method to develop their app. Here we need to specify the app that we want to create. In our case, let's create `task` app
```
python3 manage.py startapp task
```
---

## App file structure
The new apps will have files that structured like:
> project_django/
> > ... 
> > task/
> > > admin.py
> > > apps.py
> > > models.py
> > > views.py
> > > migrations/
 