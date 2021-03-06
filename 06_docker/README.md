# Welcome to the Docker module!

## Demo

### Installation
Please follow the installation instructions from here:
https://www.docker.com/get-started

### Running the demo
Please clone this repository to your local machine (or download it as a ZIP if you're not comfortable with git yet). Then, try to run the Python script in these two ways:
- `python welcome.py` - this should throw an error because of a package called `art` which you don't have locally
- `docker build . --tag docker_demo` and then `docker run docker_demo` - this should work

## Big whoop?
This might seem pointless, but something very important happened. We managed to run a piece of software on your machine without caring about having the right Python packages. Even though you don't have `art` locally, by running this file through docker, it magically works!

Docker does 'containerization' - it packages the application you want to run (the `welcome.py` script) with all its dependencies. If you inspect the `Dockerfile` you'll see that it uses an image which includes Python: `FROM python:3.8`. It also installs the `art` package using a `pip` command.

This is a very silly example, but you can package whole web applications which might include a database to store user information, a webserver, some separate system to train Machine Learning models, etc. Even in academia, instead of having Python scripts laying around which will stop working once you upgrade your OS and might not work in another researcher's machine, you can package a Jupyter Notebook into a Docker application to make sure someone else can run it.

## Tasks

### Task 1
The goal of this module is to containerize the SQL code you did before using Docker. Your application should do the following:
1. Use an appropriate `FROM` starting image.
2. Download the citations file from the webpage. Look at the Linux command `curl`: http://manpages.ubuntu.com/manpages/trusty/man1/curl.1.html
3. Create the SQL database using the code you already did before.
- Recall that you should use one of the datasets from the citation network page: https://www.aminer.org/citation. Earlier versions are smaller but use a weird file format, later versions have a better format but are larger. You choose. :)
- Then write code to create two tables:
-- One where each row is one paper (table 1)
-- One where each row is one citation (table 2)
4. Finally, use Python to query the SQL database and print the answers to the following questions. For each question, you can only use SQL, and you must use a single query for each question; you cannot run multiple queries per question.
- Which paper has the most citations? (only uses table 2)
- Which paper has the first title in alphabetical order? (only uses table 1)
- What is the title of the paper with the most citations? (needs both tables)
- Which paper grew the most in citations from one year to the next? (trickier)

Create a Dockerfile, plus any necessary extra files you need, to create the database and then execute a Python script to run SQL queries.

#### Acceptance criteria
- Your application uses Docker + some code on Github. You cannot ask people to install anything on their machines apart from Docker.
- Two other students managed to run your application without any help from you. They just read your README, clone your repo, run the appropriate `docker build` and `docker run` commands and it magically works.

## Reading materials
https://www.freecodecamp.org/news/the-docker-handbook/

### Task 2
Do the same as task 1, but use `docker-compose` to have the SQL database and the Python code as two separate applications. See more here: https://docs.docker.com/compose/
