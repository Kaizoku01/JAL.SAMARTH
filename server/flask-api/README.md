## [Flask API Server - Mongo](https://github.com/app-generator/api-server-flask-mongo)

## Table of Contents

1. [Getting Started](#getting-started)
2. [Project Structure](#project-structure)
3. [Modules](#modules)
4. [Testing](#testing)

## Getting Started

clone the project

```bash
$ git clone https://github.com/app-generator/api-server-flask-mongo.git
$ cd api-server-flask-mongo
```

create virtual environment using python3 and activate it (keep it outside our project directory)

```bash
$ python3 -m venv /path/to/your/virtual/environment
$ source <path/to/venv>/bin/activate
```

install dependencies in virtualenv

```bash
$ pip install -r requirements.txt
```

setup `flask` command for our app

```bash
$ export FLASK_APP=run.py
$ export FLASK_ENV=development
```

> Or for Windows-based systems

```powershell
$ (Windows CMD) set FLASK_APP=run.py
$ (Windows CMD) set FLASK_ENV=development
$
$ (Powershell) $env:FLASK_APP = ".\run.py"
$ (Powershell) $env:FLASK_ENV = "development"
```

start test APIs server at `localhost:5000`

```bash
$ python run.py
```

or

```bash
$ flask run
```

use `flask-restx`' swagger dashboard to test APIs, or use `POSTMAN`

## Project Structure

```bash
api-server-flask/
├── api
│   ├── config.py
│   ├── __init__.py
│   ├── models.py
│   └── routes.py
├── Dockerfile
├── README.md
├── requirements.txt
├── run.py
└── tests.py
```

<br />

## Docker

Our docker image details are in `Dockerfile`

To build the docker image (replace app name between `< >` as per your requirment)

```bash
$ docker build -t <api-server-flask-app>:latest .
```

To run the docker container

```bash
$ docker run -d -p 5000:5000 <api-server-flask-app>
```

<br />

## Modules

This application uses the following modules

- Flask==1.1.4
- flask-restx==0.4.0
- Flask-JWT-Extended
- flask-mongoengine
- pytest

## Testing

Run tests using `pytest tests.py`

<br />

---

[Flask API Server - Mongo](https://github.com/app-generator/api-server-flask-mongo) - provided by AppSeed [App Generator](https://appseed.us)
