```bash
	django.db.migrations.exceptions.InconsistentMigrationHistory: Migration admin.0001_initial is applied before its dependency app.0001_initial on database 'default'.
```

Since you are using a custom User model, you can do these 4 steps:

Comment out django.contrib.admin in your INSTALLED_APPS in settings.py:
```bash
INSTALLED_APPS = [
   ...
   #'django.contrib.admin',
   ...
]
```

Comment out the admin path in urls.py:
```bash
urlpatterns = [
   ...
   #path('admin/', admin.site.urls) 
   ...
]
```
Then run:
```bash
 python manage.py makemigrations  # (optional)
 python manage.py migrate
```
When you are done, uncomment it all back
