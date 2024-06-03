<h1 align="center">
  Spring Boot + GraphQL
</h1>

Spring Boot example with GraphQL.

## Technologies

- [Spring Boot](https://spring.io/projects/spring-boot)
- [Spring MVC](https://docs.spring.io/spring-framework/reference/web/webmvc.html)
- [Spring for GraphQL](https://spring.io/projects/spring-graphql)

## How to execute

- Start your Spring application

## Enter in the GraphiQL Playground

GraphiQL is a useful visual interface for writing and executing queries.

### Run the query

```
query bookDetails {
  bookById(id: "book-1") {
    id
    name
    pageCount
    author {
      id
      firstName
      lastName
    }
  }
}
```

### You should get the response above

```
{
  "data": {
    "bookById": {
      "id": "book-1",
      "name": "Effective Java",
      "pageCount": 416,
      "author": {
        "id": "author-1",
        "firstName": "Joshua",
        "lastName": "Bloch"
      }
    }
  }
}
```