# Backend tester
## What is this?
This is my personal project following allowing with a django framework API course to create RESTful APIs that can communicate with a frontend server.
Planning to connect this up to VUE & MySQL, which will probably be seen in other github projects too

## What is the technologies being used?
- Python
- DJango
- DJANGO REST framework
- PostgreSQL
- Docker
- Swagger (automated API docs)
- Github (ofc)

## What practices are going to be used?
Test Driven Decelopment (TDD)
- Writing tests before implementation

## Building images
run 'docker-compose build'
<s>run 'docker build .' </s>

## linting
Running flake8:
    docker-compose run --rm app sh -c "flake8"

## creating python app
docker-compose run --rm app sh -c "django startproject app ."

## starting a container
docker-compose up

## (TDD) adding features to app
 1. Add test to the tests.py file for expected input & output
 2. add the functionality

## mocking

Removal of external dependencies on tests:
overide externalisation & sleep function code

### how to do it?

Use [unittest.mock](https://docs.python.org/3/library/unittest.mock.html) library

## tests
### Running
python manage.py test

using the docker file:
    docker-compose run --rm app sh -c "python manage.py test"

### Creating tests
In the app add 'tests.py' file
now just copy the setup.
dont forget 'test_' for all test methods
Use 'self.assertEqual(res,value)' at the end of the method to do the unit test check

### API

Djangorestframework:
    In `tests.py` use:
    `from rest_framework.tests import APIClient`
    within the test method run:
    `client = APIClient()`
    `res = client.{get,push, etc.}('api url')`

### Trouble shooting
#### Tests arent running
1. Ensure `__init__.py` is there in the same folder of `tests.py`
2. Ensure indentations are correct
3. ensure the `test` have the `test_` prefix
   
### Import errors
1. check there isn't both a `tests` directory and `tests.py` file

## volumes
Persistent data, found in official docs of whatever DB ur using