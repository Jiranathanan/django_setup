# Installing new Python version on MacOS Catalina (For Django 5.x)
## download from [https://www.python.org/downloads/](https://www.python.org/downloads/)
### After install: Check that it works:
```bash
python3.13 --version
```
# Create a venv Using That Python Version
```bash
python3.13 -m venv myenv
```

# Activate the Virtual Environment
```bash
source myenv/bin/activate
```
Then confirm:
```bash
python --version
```

# Install the Latest Django
```bash
pip install django
```
check version
```bash
django-admin --version
```

