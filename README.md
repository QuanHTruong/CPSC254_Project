# CPSC254_Project
CPSC 254 Open-Source Software Development Project
Food tracker and Calories tracker

Install the following prerequisites:

1. [Python 3.8-3.11](https://www.python.org/downloads/)
<br> This project uses **Django v4.2.4**. For Django to work, you must install a correct version of Python on your machine. More information [here](https://django.readthedocs.io/en/stable/faq/install.html).
2. [PostgreSQL](https://www.postgresql.org/download/)
3. [Visual Studio Code](https://code.visualstudio.com/download)

## Installation
### 1. Install allthe required libaries
pip install -r requirements.txt

### 2. Set up PostgreSQL database

With **PostgreSQL** up and running, in a new Terminal window, run:

```bash
dropdb --if-exists food
```

Start **psql**, which is a terminal-based front-end to PostgreSQL, by running the command:

```bash
psql postgres
```

Create a new PostgreSQL database:

```sql
CREATE DATABASE food;
```

Create a new database admin user:

```sql
CREATE USER yourusername WITH SUPERUSER PASSWORD 'yourpassword';
```

To quit **psql**, run:

```bash
\q
``` 
### 3. Set up .env
SECRET_KEY=yoursecretkey
DEBUG=True
DATABASE_NAME=food
DATABASE_USER=yourusername
DATABASE_PASS=yourpassword
DATABASE_HOST=localhost 

### 4.Run migration 
```bash
python manage.py makemigrations
```

```bash
python manage.py migrate
``` 

