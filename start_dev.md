```bash
	# install django
	poetry add django
	# create project
	poetry run django-admin startproject djangocourse . # add . to tell poetry to create project using current folder
	# start server
	poetry run python ./manage.py runserver

	# Access Admin Panel
	# run migration and create admin superuser that has acess to the admin panel
	poetry run python ./manage.py migrate 
	# that command will modify our data using pre-existing migration

	# create superuser
	poetry run python ./manage.py createsuperuser
```
