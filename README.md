#Project Under Development

# Project Setup Guide

## Setting Up the Project

Follow these steps to get the Django project up and running.

### 1. Install Python and pip

Make sure Python 3 and pip (Python's package installer) are installed.

#### Check if Python is installed:
```bash
python3 --version
```

If Python is not installed, run:
```bash
sudo apt update
sudo apt install python3 python3-pip python3-venv
```

2. Set Up a Virtual Environment (Optional but Recommended)
Create a virtual environment:
```bash
python3 -m venv myenv
```

Activate the virtual environment:
```bash
source myenv/bin/activate
```

Your terminal prompt should now show (myenv) indicating the environment is active.

3. Install Project Dependencies
Install Django manually:
```bash
pip install django
```

4. Install Dependencies 
For Crispy Forms:
```bash
pip install django-crispy-forms
```
For Crispy Forms bootstrap:
```bash
pip install crispy-bootstrap4
```

8. Run the Development Server
To start the development server, run:
```bash
python manage.py runserver
```

#Your project will be accessible at http://127.0.0.1:8000/.
