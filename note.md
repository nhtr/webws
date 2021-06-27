## database setup

###go to `app-name/settings.py`
- `django.contrib.admin` – The admin site. You’ll use it shortly.
- `django.contrib.auth` – An authentication system.
- `django.contrib.contenttypes` – A framework for content types.
- `django.contrib.sessions` – A session framework.
- `django.contrib.messages` – A messaging framework.
- `django.contrib.staticfiles` – A framework for managing static files.
###to create the tables in the database run command
`python manage.py migrate`
### create model
edit in `polls/models.py`
###Activating models
Edit the `app-name/settings.py` file and add that dotted path to the `INSTALLED_APPS` setting
The sqlmigrate command takes migration names and returns their SQL
`python manage.py sqlmigrate polls 0001`
Now, run migrate again to create those model tables in your database:
`python manage.py migrate`
###Creating an admin user
Run command `python manage.py createsuperuser`
###Start the development server
Run command `python manage.py runserver`
###Django’s generic views
- Each generic view needs to know what model it will be acting upon. This is provided using the model attribute.
- The DetailView generic view expects the primary key value captured from the URL to be called "pk", so we’ve changed question_id to pk for the generic views.
- More [generic views documentation]('https://docs.djangoproject.com/en/3.2/topics/class-based-views/')