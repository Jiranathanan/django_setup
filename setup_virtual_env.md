# Django Project Setup Without Poetry, Pipx, or Pyenv (macOS Catalina Compatible)

This guide helps you set up a Django development environment on macOS Catalina **without using Poetry, pipx, or pyenv**. Instead, we use Python's built-in `venv` and `pip` tools.

---

## ✅ Step 1: Set Up the Project Folder

Make sure you're in the root folder of your Django project. This folder should contain:

```
README.md
your_project/
tests/
```

Open this folder in Visual Studio Code.

---

## ✅ Step 2: Create a Virtual Environment

If you installed Python 3.10+ manually (e.g., from Python.org), run:

```bash
python3.11 -m venv .venv
```

This creates a `.venv/` folder in your project directory.

---

## ✅ Step 3: Activate the Virtual Environment

```bash
source .venv/bin/activate
```

You should now see your terminal prompt change to indicate you're in the `.venv` environment.

---

## ✅ Step 4: Select the Interpreter in VS Code

1. Open the Command Palette: `Cmd + Shift + P`
2. Type: `Python: Select Interpreter`
3. Choose: `Enter interpreter path`
4. Point it to:
   ```
   ./.venv/bin/python
   ```
   Or provide the full absolute path if needed:
   ```
   /Users/yourname/path/to/project/.venv/bin/python
   ```

---

## ✅ Step 5: Install Django

With the virtual environment activated:

```bash
pip install django
```

This installs the latest version (e.g., Django 5.1.5).

---

## ✅ Step 6: Lock Dependencies (Optional but Recommended)

Freeze your dependencies into a requirements file:

```bash
pip freeze > requirements.txt
```

Others can install them via:

```bash
pip install -r requirements.txt
```

---

## ✅ Optional: Pin Django Version

To ensure future installs don't accidentally upgrade to Django 6.x:

```bash
pip install "django>=5.1.5,<6"
```

Then update your `requirements.txt`:

```bash
pip freeze > requirements.txt
```

---

## ✅ Summary

| **Poetry Command**          | **Manual Alternative**                               |
| --------------------------- | ---------------------------------------------------- |
| `poetry install --no-root`  | `python3 -m venv .venv && source .venv/bin/activate` |
| `poetry add django`         | `pip install django`                                 |
| `pyproject.toml`, lock file | `requirements.txt` via `pip freeze`                  |
| Poetry-managed interpreter  | Set manually in VS Code via `.venv/bin/python`       |

---

This setup gives you full control without relying on tools that may not work on older macOS versions.

