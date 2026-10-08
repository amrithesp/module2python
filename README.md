# Python Project Setup

## Project Overview

This project demonstrates the basic setup of a Python project using a virtual environment, project dependencies, Git, and a `.gitignore` file.

## Virtual Environment

A virtual environment is used to create an isolated Python environment for the project. It allows the project to have its own Python interpreter and installed packages without affecting other Python projects or the system Python environment.

### Create the virtual environment

powershell
python -m venv venv

### Activate the virtual environment

powershell
.\venv\Scripts\Activate.ps1

After activation, the terminal displays `(venv)` before the PowerShell prompt.

### Install dependencies

powershell
python -m pip install -r requirements.txt


## Checking the Python Path

The following command shows which Python executable is being used:

powershell
python -c "import sys; print(sys.executable)"


When the virtual environment is activated, the Python executable comes from:

text
venv\Scripts\python.exe


When the virtual environment is not activated, Python uses the system Python installation.

This demonstrates that the virtual environment provides an isolated Python environment for the project.

## Requirements

The `requirements.txt` file contains the Python packages required by the project, including their versions.

Dependencies can be installed using:

powershell
python -m pip install -r requirements.txt


## Git and .gitignore

Git is used for version control.

The `.gitignore` file prevents unnecessary files from being committed to the repository.

The project ignores:

text
venv/
__pycache__/
*.pyc

The virtual environment is not committed because it is machine-specific and can be recreated using the `venv` command.

## Interview Explanation

A virtual environment is useful because different Python projects may require different versions of the same package. By creating a separate environment for each project, dependency conflicts can be avoided.

For example, one project may require one version of a package while another project may require a different version. Each virtual environment keeps these dependencies separate.

Therefore, virtual environments make Python projects easier to manage, reproduce, and maintain.
