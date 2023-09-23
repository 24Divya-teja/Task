# TaskMate
Heres a basic to do list to keep you accountable of your tasks. Simply register your own user, create a task with a title, due date and description. Each task can have comments made.

When your task is overdue, you will see an "Overdue" message displayed, along with an increment of the overdue task counter in the UI. Once completed, move the task to Done. Otherwise, Delete the task to be lost forever.


## Features

- Multitenancy with a shared database schema
- Basic Authentication
- Secure session management protected by IP and login device
- Written in Flask with gunicorn for performance
- Feature rich To Do list
- Easy ability to self host via cli or Docker
- Application wide logging
- Clean and simple UI
- Postgres, SQLite support
- Timezone support

## Setup
Initialise the database and virtual environment. 
🚨 Please note that psycopg2 is needed for ```make db``` but needs to be removed when building the Docker image.

```bash
  virtualenv venv
  source venv/bin/active
  venv/bin/pip install -r requirements.txt
  make env db 
```

Please change any values needed in ```.env```


## Run locally
Run with the ```Makefile```
```bash
  make run
```

You can run with debug mode enabled with the ```Makefile```
```bash
  make debug
```
## Building the Docker image
Run with the ```Makefile```
```bash
  make build
```
## Docker

#### Run with docker-compose (development environment)

```bash
  make docker-dev
```
Please change any values needed in ```.env``` and ```docker-compose/docker-compose-dev.yaml```


#### Run with docker-compose (production environment)

```bash
  make docker
```
Please change any values needed in ```.env``` and ```docker-compose/docker-compose.yaml```


## Testing

Run Pytest against the code, including test coverage

```bash
  make test sast
```

## Authors

- [@Divya](https://github.com/24Divya-teja/Task/tree/main)

## Screenshots
### Creating a task:

![](/screenshots/create-task.png)

### Active tasks:

![](/screenshots/active-tasks.png)

### Done tasks:

![](/screenshots/done-tasks.png)

### First view upon login:

![](/screenshots/first-login.png)