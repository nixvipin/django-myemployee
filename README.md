Django Employee APP

Employee Management application written in Pyhon (Django).

Components:

    admin panel to manage employees' data
    API to list, add and remove employees

Note: to run the app using Docker, head over README-docker.md

Build Status codebeat badge codecov Dependency Status

Pre-requisites:

    python3 (v3.5)
    python-pip3 (v9.0.1)

Install dependencies

pip3 install -r requirements.txt
pip3 install -r requirements-test.txt

Go to employeemanager directory

Before running any of the following commands, you should cd into employeemanager directory:

cd employeemanager

Run migrations

python manage.py migrate

Create superuser with privileged access

python manage.py createsuperuser

Test

coverage run --source='.' manage.py test staff.tests

Code coverage report

Note: Run this command only after running the test suite with the command above.

coverage html
# the report will be located at `htmlcov/index.html`

Start app

python3 manage.py runserver localhost:8000

API usage

To interact with the API, log in at http://localhost:8000/staff/api-auth/ with the superuser created before. After log in, you might be redirected to an interactive interface.
Admin

Head over http://localhost:8000/staff/admin/ to access the admin.
