# Install Django Without Poetry

## 1. 🔒 Create a Virtual Environment
This keeps your Django project isolated (no global mess).

```bash
python3 -m venv env
source env/bin/activate   # on macOS/Linux
```
You’ll know it’s active when your terminal prompt shows `(env)`.

---

## 2. 📦 Install Django via pip
Now install Django directly:

```bash
pip install django
```

Check the version:

```bash
django-admin --version
```

---

## 3. 🏗️ Create a Django Project

```bash
django-admin startproject mysite .
```
This creates your Django project in the current directory.

---

## 4. 🚀 Run the Development Server

```bash
python manage.py runserver
```

Then open your browser and go to:

```
http://127.0.0.1:8000
```

---

## 5. (Optional) Create a Django App

```bash
python manage.py startapp myapp
```

This sets up a Django app inside your project directory.

