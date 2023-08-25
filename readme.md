# Bookstore Application

This is a Django-based web application for managing a bookstore. It provides functionality for user authentication, book management, and other core features required for running an online bookstore.

## Features

- User authentication and registration with Django Allauth
- Book management system
- Admin panel for managing content
- Custom user model
- Debug toolbar for development

## Technology Stack

- **Backend:** Django 4.2
- **Database:** PostgreSQL
- **Frontend:** Bootstrap 5 with Crispy Forms
- **Authentication:** Django Allauth
- **Environment Management:** Environs
- **Development Tools:** Django Debug Toolbar

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/bookstore.git
   cd bookstore
   ```

2. **Create a virtual environment and activate it:**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install the required packages:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Set up the environment variables:**
   Create a `.env` file in the root directory and add the following variables:

   ```env
   DJANGO_SECRET_KEY=your_secret_key
   DJANGO_DEBUG=True  # Set to False in production
   DJANGO_SECURE_SSL_REDIRECT=True
   DJANGO_SECURE_HSTS_SECONDS=2592000
   DJANGO_SECURE_HSTS_INCLUDE_SUBDOMAINS=True
   DJANGO_SECURE_HSTS_PRELOAD=True
   DJANGO_SESSION_COOKIE_SECURE=True
   DJANGO_CSRF_COOKIE_SECURE=True
   ```

5. **Apply migrations:**

   ```bash
   python manage.py migrate
   ```

6. **Create a superuser:**

   ```bash
   python manage.py createsuperuser
   ```

7. **Run the development server:**
   ```bash
   python manage.py runserver
   ```

## Configuration

### Database

The application uses PostgreSQL. Update the database settings in `settings.py` if necessary:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'bookstore',
        'USER': 'postgres',
        'PASSWORD': 'postgres',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}

```

### Static and Media Files

- Static files are located in the static/ directory.
- Media files are located in the media/ directory.

## Running Tests

To run tests, use the following command:

```bash
python manage.py test
```

## Deployment

For deployment, ensure that the environment variables are properly set and debug mode is turned off. Use a WSGI server like Gunicorn and a web server like Nginx for serving the application.
