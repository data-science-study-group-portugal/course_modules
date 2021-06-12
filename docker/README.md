# Welcome to the Docker module!

## Instructions
Please clone this folder to your local machine (or download it as a ZIP if you're not comfortable with git yet). Then, try to run the Python script in these two ways:
- `python welcome.py` - this should throw an error because of a package called `art` which you don't have locally
- `docker build . --tag docker_demo` and then `docker run docker_demo` - this should work

## Big whoop?
This might seem pointless, but something very important happened. We managed to run a piece of software on your machine without caring about having the right Python packages. Even though you don't have `art` locally, by running this file through docker, it magically works!

Docker does 'containerization' - it packages the application you want to run (the `welcome.py` script) with all its dependencies. If you inspect the `Dockerfile` you'll see that it uses an image which includes Python: `FROM python:3.8`. It also installs the `art` package using a `pip` command.

This is a very silly example, but you can package whole web applications which might include a database to store user information, a webserver. Even in academia, instead of having Python scripts laying around which will stop working once you upgrade your OS and might not work in another researcher's machine, you can package a Jupyter Notebook 

# Tasks

## Task 1
The goal of this module is to containerize the SQL code you did before. Create a Dockerfile, plus any necessary extra files you need, to create the database and then execute a Python script to run SQL queries.

### Acceptance criteria
Two other students managed to run your notebook without any help from you. They just read your README, clone your repo, and it magically works.
