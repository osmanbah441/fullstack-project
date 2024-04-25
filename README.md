
# Restaurant Reservation System

This is a full-stack Django application that allows users to book reservations at a restaurant. It uses a MySQL database to store booking information.

**Technologies:**

- Python 3.10.X
- Django (Recommended: Use a virtual environment manager like `pipenv`)
- MySQL (Install using `sudo apt install mysql-server` on Ubuntu)

**Installation:**

1. **Clone the Repository:**

   ```bash
   cd fullstack-project
   ```
Create a Virtual Environment (Recommended):

```bash
pipenv shell
pipenv install

# This will create a virtual environment and install the required dependencies listed in Pipfile.
```
Install MySQL Dependencies (if not already installed):

```bash
# on ubuntu make sure to install this
sudo apt install libmysqlclient-dev
```

If you're not using the default MySQL configuration, update the database settings in settings.py:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'your_database_name',
        'USER': 'your_database_user',
        'PASSWORD': 'your_database_password',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
```

Apply Database Migrations:

```bash
pipenv run python manage.py makemigrations
pipenv run python manage.py migrate
```


Run the Development Server:

```Bash
python manage.py runserver
```

User Guide:

Making Reservations:
Navigate to the book tab.

Browse available dates and times for reservations.
Select the desired date and time slot.
Enter the number of guests in your party.
Submit your reservation request.
