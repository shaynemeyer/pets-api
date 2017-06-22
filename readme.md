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

```

## Resources

* [Flask Pluggable Views](http://flask.pocoo.org/docs/0.12/views/)
* [http status codes](http://www.restapitutorial.com/httpstatuscodes.html)