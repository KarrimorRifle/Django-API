# APPLICATION
## Start up
'docker-compose up' in the same dir as .yml

## Connectin
use localhost:8000

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