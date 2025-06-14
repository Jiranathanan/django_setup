# install pyenv from

https://github.com/pyenv-win/pyenv-win

Windowns (powershell)
```
Invoke-WebRequest -UseBasicParsing -Uri "https://raw.githubusercontent.com/pyenv-win/pyenv-win/master/pyenv-win/install-pyenv-win.ps1" -OutFile "./install-pyenv-win.ps1"; &"./install-pyenv-win.ps1"
```

Run 
```bash
pyenv --version to check if the installation was successful
```
Run 
```bash
pyenv install -l to check a list of Python verison support by pyenv-win
```
Run 
```bash
pyenv install <version> to install the supported version
```
Run 
```bash
pyenv global <version> to set s Python version as the global version

pyenv exec pip install --user pipx
pyenv exec pipx ensurepath -- force

pipx install poetry
poetry new djangocourse
```
