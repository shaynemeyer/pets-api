# Pets API
A REST API example written in Python and Flask.



## Build the Docker Containers
```bash
docker-compose build
```

## Start mongodb separately
```bash
docker-compose up -d db
```

## Start the app: 
```bash
docker-compose up web
```

## Login to MongoDB console from web app
```
docker exec -it petsapi_web_1 mongo -host mongodb
```

## Run tests in docker container
```bash
docker exec -it petsapi_web_1 python3 tests.py
```

## Import data

### Login to shell
```
docker exec -it petsapi_web_1 python3 manage.py shell
```

### Once you have a shell, load the models
```
from store.models import Store
from pet.models import Pet
```

### Delete any existing Stores and Pets
```
Store.objects.all().delete()
Pet.objects.all().delete()
```

### Import Stores
```
from application import fixtures
fixtures('pets-api', 'store', 'store/fixtures/stores.json')
```
### Import Pets
```
fixtures('pets-api', 'pet', 'pet/fixtures/pets.json')
```
## Resources

* [Flask Pluggable Views](http://flask.pocoo.org/docs/0.12/views/)
* [http status codes](http://www.restapitutorial.com/httpstatuscodes.html)