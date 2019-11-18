# Movies Api - Graphql & Typescript CRUD

Experimental Movie Api built with:

- typeorm
- type-graphql
- apollo-graphql
- sqlite
- express
- typescript


## Usage

### Queries
Get all movies

```gql
{
  movies{
    id
    title
    minutes
  }
}
```

Get a Movie by id


```gql
{
  movie(id: 2) {
    title
    minutes
  }
}
```

Greetings :D

```gql
{
  hello
}
```

### Mutations
Capable of creating, updating and deleting a movie.

#### Create a Movie
Creates a movie and returns it.

```gql
mutation{
  createMovie(options:{
    title:"Titanic",
    minutes: 120
  }){
    id
    title 
    minutes
  }
}
```

#### Delete a Movie
Deletes a movie and returns true.

```gql
mutation{
  deleteMovie(id:3)
}
```

#### Update a Movie
Updates a movie and returns true.

```gql
mutation {
  updateMovie(id: 2, input: { title: "Titanic 2" })
}
```

