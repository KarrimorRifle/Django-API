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