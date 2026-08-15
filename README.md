# Inkora - Django Blog Project

A simple blog website built with **Django** and **PostgreSQL** for the Simple Blog project requirements.

## Project requirements covered

- User registration and login
- Home page showing posts
- Post page with title, body, and all comments
- Logged-in users can add comments
- Logged-in users can create new posts
- PostgreSQL database
- Django Models with one-to-many relationships

## Pages

1. Home page
2. Post details page
3. Registration page
4. Login page
5. Add New Post page

## Database structure

- **User:** email, name, gender, address
- **Post:** title, body, user
- **Comment:** body, user, post

A user can write many posts and many comments. A post can contain many comments.

## Setup

### 1. Create PostgreSQL database

Create a database named `simple_blog_db` in PostgreSQL.

### 2. Configure database

The project reads these environment variables when available:

- `DB_NAME`
- `DB_USER`
- `DB_PASSWORD`
- `DB_HOST`
- `DB_PORT`

The default values are suitable for a local PostgreSQL installation and can be changed in `simple_blog/settings.py`.

### 3. Install packages

```bash
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

### 4. Apply migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

### 5. Create an admin user (optional)

```bash
python manage.py createsuperuser
```

### 6. Run the project

```bash
python manage.py runserver
```

Open `http://127.0.0.1:8000/` in your browser.

## Admin

Open `http://127.0.0.1:8000/admin/` after creating a superuser. Users, posts, and comments are available from the Django admin panel.
