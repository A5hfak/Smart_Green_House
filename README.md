# Project Setup Guide

## Setting Up the Project on a Fresh Linux Machine

Follow these steps to get your Django project up and running on a freshly installed Linux machine.

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
Creating a virtual environment isolates project dependencies and ensures compatibility.

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
If you're using a requirements.txt file, install all dependencies:
```bash
pip install -r requirements.txt
```
Alternatively, if you want to install Django manually:
```bash
pip install django
```
If you're using a specific database (e.g., PostgreSQL, MySQL), you may need to install additional dependencies (see next steps).

4. Install Database Dependencies (if needed)
If you're using PostgreSQL, MySQL, or another database, you'll need the appropriate adapter.

For PostgreSQL:
```bash
sudo apt install libpq-dev
pip install psycopg2
```
For MySQL:
```bash
sudo apt install libmysqlclient-dev
pip install mysqlclient
```
For SQLite (default):
No extra installation is required for SQLite since it’s bundled with Python. However, if you need the SQLite libraries:
```bash
sudo apt install sqlite3 libsqlite3-dev
```

5. Set Up the Database
For PostgreSQL:
Create a new database:
```bash
sudo -u postgres createdb mydatabase
```
For MySQL:
Create a new database:
```bash
mysql -u root -p
```
CREATE DATABASE mydatabase;
If you are using SQLite, no setup is required as it is file-based.

6. Apply Database Migrations
Run migrations to set up your database schema:
```bash
python manage.py migrate
```

7. Create a Superuser (Optional)
To access the Django admin panel, create a superuser:
```bash
python manage.py createsuperuser
```
Follow the prompts to set up the username, email, and password.

8. Run the Development Server
To start the development server, run:
```bash
python manage.py runserver
```

#Your project will be accessible at http://127.0.0.1:8000/.
