# ForumFy
Single-page forum application built in ReactJS and Django Rest Framework.


## Frontend
> The frontend is a fast, interactive and simple Single-Page-Application (SPA), written in ES6 Javascript and built with following technologies:
> * [React v16]
> * [Redux v4]
> * [React Router v4]
> * [Redux Thunk v2]
> * [Redux Persist v5.]


## Backend
> The backend is a scalable system that provides data through its RESTful API (browseable API available), written in Python and built with following technologies:
> * [Django]
> * [Djangorestframework]

## API endpoint
```
List of available API (browseable) at /api
* /user/
* /user/login/
* /user/register/
* /user/logout/
* /user/{username}/
* /user/{username}/edit
* /user/{username}/delete
* /forum/
* /forum/create/
* /forum/{slug}/
* /forum/{slug}/edit/
* /forum/{slug}/delete/
* /thread/
* /thread/create/
* /thread/{id}/
* /thread/{id}/edit/
* /thread/{id}/delete/
* /post/
* /post/create/
* /post/{id}/
* /post/{id}/edit/
* /post/{id}/delete/
```

## Installation

Make sure you have following software installed in your system:
* Python 
* Node.js
* NPM / Yarn
* Git

First, we need to clone the repository
```
git clone https://github.com/sss3322/Online-Forum.git
```

Install all required dependencies in an isolated environment

```
cd backend
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

Copy the `.env.example` as `.env` in `backend` folder
```
copy .env.example .env
```

Install all required dependencies for frontend in ForumFy/frontend folder by typing
```
cd ../frontend
yarn
```

Copy the `.env.example` as `.env` in `frontend` folder
```
copy .env.example .env
```

## Running Backend on Local Server

Activate virtual environment

```
cd backend
venv\Scripts\activate
```

(Optional) Run test
```
python manage.py test
```

Then run the server, api endpoint should be available on http://localhost:8000/api

```
python manage.py runserver
```

## Running Frontend on Local Server

Start development server

```
cd frontend
yarn start
```

Frontend should be available on http://localhost:3000/

### Test User
By default, the database for development server in `backend/db.sqlite3` is already filled with some data for ease of development. The superuser id is `suchithra` and password is `suchithra332` as well.

If you want to start clean. Delete `db.sqlite3` and follow this step in `backend folder`
```py
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
```
