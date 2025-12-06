# Django Boilerplate - Simple Ajax CRUD

A simple Django application based on [How to Implement CRUD Using Ajax and Json](https://simpleisbetterthancomplex.com/tutorial/2016/11/15/how-to-implement-a-crud-using-ajax-and-json.html) with added Google Maps functionality.

## Requirements

- Python 3.11+
- Django 4.2.27
- MySQL/MariaDBS

## Running Locally

### 1. Clone the repository

```bash
git clone https://github.com/scedar/django_boilerplate.git
cd django_boilerplate
```

### 2. Create and activate a virtual environment

```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure environment variables

Copy the example environment file and update it with your configuration:

```bash
cp .env.example .env
```

Edit `.env` and set your values:

```env
SECRET_KEY=your-secret-key-here
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1

DB_NAME=django_boilerplate_db
DB_USER=root
DB_PASSWORD=your-database-password
DB_HOST=localhost
DB_PORT=3306

GEOPOSITION_GOOGLE_MAPS_API_KEY=your-google-maps-api-key
```

**Get a Google Maps API key:** https://developers.google.com/maps/documentation/javascript/get-api-key

### 5. Set up the database

Create the database:

```bash
mysql -u root -p -e "CREATE DATABASE django_boilerplate_db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;"
```

Run migrations:

```bash
python manage.py makemigrations books
python manage.py migrate
```

### 6. Run the development server

```bash
python manage.py runserver
```

Visit http://localhost:8000 in your browser.

## References

* [How to Implement CRUD Using Ajax and Json](https://simpleisbetterthancomplex.com/tutorial/2016/11/15/how-to-implement-a-crud-using-ajax-and-json.html)
* [django-geoposition-2](https://github.com/blueshiftlabs/django-geoposition) - Maintained fork
* [Django Documentation](https://docs.djangoproject.com/)

## Authors

* **Ochomo William** - [ochomoswill](https://ochomoswill.github.io/) - Member of [Scedar Technologies Co.](https://scedar.bitbucket.io/)
