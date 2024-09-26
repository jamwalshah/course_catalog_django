# course_catalog_django

- This is a mini-project developed to showcase the Django framework skills using CRUD operations on MySQL database from a Python Django based app
- It'll read records from the database and show all the existing courses in a tabular format on the index/homepage
- You may create a new course, update/delete an existing one from the index/homepage itself

## Setting up the environment

- You have a file `requirements.txt` that can be used to fulfil requirements of this project
- You need to have MySQL installed for database storage purpose

### Steps to set-up python environment from `requirements.txt`

1. Open cmd and navigate to the repo path
2. Then create an environment named `env` using command below in cmd (it's specific to windows, Linux/Mac users need to format these commands as per their OS)

    ```bash
    python -m venv env
    ```

3. Then activate this environment `env` using command below in cmd

    ```bash
    env\Scripts\activate
    ```

4. Once virtual environment `env` is activated, run command below to install all the requirements

    ```bash
    pip install -r requirements.txt
    ```

### Steps to set-up MySQL

1. You need to create a file `courseProject/.env` for the database credentials in the format below, which will be used to connect to MySQL database

    ```text
    DB_NAME=your_database_name
    DB_USER=your_database_username
    DB_PASSWORD=your_database_password
    ```

2. You need to connect to MySQL (You may use MySQL Workbench or MySQL interactive command-line), and run the command below to create a database you'll use with the app (Replace the database name with what you've specified in `courseProject/.env`)

    ```sql
    CREATE DATABASE your_database_name;
    ```

## Running the Project

- Make sure that MySQL database service is up and running
- The Project files are in `courseProject` directory in this repo

1. Change directory to `courseProject`

    ```bash
    cd courseProject
    ```

2. In `courseProject` directory, you have `manage.py` file which is an entry point for Django projects.
3. You need to do the migrations, so run the two commands below

    ```bash
    python manage.py makemigrations
    ```

    ```bash
    python manage.py migrate
    ```

4. To run the Django Server for this Django project, use command

    ```bash
    python manage.py runserver
    ```

5. Once your Django project is running without any error, open the web-browser and visit the URL at `localhost:8000` to play around with the project

### Stopping the project

- It is very simple, On the command-line where you've started the project, just exit it using `Ctrl+C`

## Project Highlights

1. Focus has been on documentation and industry standard coding practices
2. Idea is to demonstrate the functionality of CRUD operations, although it lacks on the UI front
3. Virtual Environment has been used to isolate this project environment
4. Database Connectivity using MySQL database in Django Framework is demonstrated
5. Credentials has been ignored from the commits using `.gitignore`, if someone has to run on their machine, you've to setup their own `.env` file and you're good to go
