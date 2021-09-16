# Django🐍

> Django is a high-level Python web framework that encourages rapid development and clean, pragmatic design. Built by experienced developers, it takes care of much of the hassle of web development, so you can focus on writing your app without needing to reinvent the wheel. It’s free and open source.


### Main features

* Separated dev and production settings

* Example app with custom user model

* SQLite by default if no env variable is set

# Usage

To use this template to start your own project:

### Existing virtualenv

If your project is already in an existing python3 virtualenv first install django by running

    $ pip install django
    
And then run the `django-admin.py` command to start the new project:

    $ django-admin.py startproject \
      --template=https://github.com/nikola-k/django-template/zipball/master \
      --extension=py,md \
      <project_name>
      
### No virtualenv

This assumes that `python3` is linked to valid installation of python 3 and that `pip` is installed and `pip3`is valid
for installing python 3 packages.

Installing inside virtualenv is recommended, however you can start your project without virtualenv too.

If you don't have django installed for python 3 then run:

    $ pip3 install django
    
And then:

    $ python3 -m django startproject <project_name>
      
      
After that just install the local dependencies, run migrations, and start the server.

### Add Basic URLs and Views
1. Map your Project’s urls.py file to the new app.
2. In your App directory, create a urls.py file to define your App’s URLs.
3. Add views, associated with the URLs, in your App’s views.py; make sure they return a HttpResponse object. Depending on the situation, you may also need to query the model (database) to get the required data back requested by the end user.


### Templates and Static Files
1. Create a templates and static directory within your project root.
2. Update settings.py to include the paths to your templates.
3. Add a template (HTML file) to the templates directory. Within that file, you can include the static file with - <pre>{% load static %}</pre> and <pre> {% static "filename" %} </pre>. Also, you may need to pass in data requested by the user.
4. Update the views.py file as necessary.


### Models and Databases

1. Update the database engine to settings.py (if necessary, as it defaults to SQLite).
2. Create and apply a new migration.
3. Create a super user.
4. Add an admin.py file in each App that you want access to in the Admin.
5. Create your models for each App.
6. Create and apply a new migration. (Do this whenever you make any change to a model).


### Forms
1. Create a forms.py file at the App to define form-related classes; define your ModelForm classes here.
2. Add or update a view for handling the form logic - e.g., displaying the form, saving the form data, alerting the user about validation errors, etc.
3. Add or update a template to display the form.
4. Add a urlpattern in the App’s urls.py file for the new view.

### User Registration
1. Create a UserForm
2. Add a view for creating a new user.
3. Add a template to display the form.
4. Add a urlpattern for the new view.

### User Login
1. Add a view for handling user credentials.
2. Create a template to display a login form.
3. Add a urlpattern for the new view.

### Setup the template structure
1. Find the common parts of each page (i.e., header, sidebar, footer).
2. Add these parts to a base template
3. Create specific. templates that inherent from the base template.
