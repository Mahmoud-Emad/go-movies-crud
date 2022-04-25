# Movie system
Example microservice written in Go-Lang.

#### Table of Contents  
* [Endpoints](#endpoints)
* [Tests](#tests)
* [Libraries](#libraries)
    *  [http](#http)  
    *  [gorilla](#doobie)

## Endpoints
The rest endpoints listed below:

Method | Url          | Description
------ | -----------  | -----------
GET    | /movies      | Returns all movies.
GET    | /movies/{id} | Returns movie for given id. Returns 404 when movie with passed id does not exist
POST   | /movies      | Creates a movies. Pass movie title and director in JSON body. Returns a 201 with the created movie.
PUT    | /movies/{id} | Updates an existing movie. Pass movie title and director in JSON body. Returns a 200 with the updated movie when a movie is present with the specified id, 404 otherwise.
DELETE | /movies/{id} | Deletes the movie with the specified id. Returns 404 when no movie present with passed id.
<!-- 
Some example requests: 

Get all movies from external recommendation system:
```curl http://localhost:8080/allMovies```

Create a movie:
```curl -X POST --header "Content-Type: application/json" --data '{"title": "Star Wars IV", "rate": "Good"}' http://localhost:8080/movies```

Get all movies from your local storage:
```curl http://localhost:8080/movies```

Get a single movie (assuming the id of the movie is 1):
```curl http://localhost:8080/movies/1```

Update a movie (assuming the id of the movie is 1):
```curl -X PUT --header "Content-Type: application/json" --data '{"title": "Star Wars IV"", "rate": "Good"}' http://localhost:8080/movies/1```

Delete a movie (assuming the id of the movie is 1):
```curl -X DELETE http://localhost:8080/movies/1``` -->

<!-- ## Tests
For testing purposes I use ScalaTest. Unit tests are using mocks, while integration tests are using real HTTP client to make requests.
To run unit tests do `sbt test`. To run integration tests `sbt it:test`. -->

## Possible improvements
- [ ] Add Swagger integration for API documenting 
- [ ] Add SQL syntax checks
- [ ] Add continuous integration
- [ ] Dockerize the application
- [ ] Add logging mechanism
- [ ] Add property based testing