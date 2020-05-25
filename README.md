# Microservices-basics

## what is a microservice?

In a monolithic server, contains routing middlewares,business logic and database access to implement all features of our app.
Eg: req-> authmiddleware->router->all feature controllers -> database

In a Micro server, contains routing middlewares,business logic and database access to implement ONE features of our app.
Eg: req-> authmiddleware->router->one feature controller -> its own database


## challenges
#### 1 Data management between services
with microservices, we store and access data in sort of starnge way
- how we store data
- how we access it
rules:-
- each service gets its own database
- services will never ever reach into another services database

#### why database-per-service
- we want each service to run independently of other services
- Database schema/structure might change unexpectedly
- some services might function more efficiently with different types of DB's(SQL vs noSQL)

#### communication between services
Sync - services communicate with each other using direct requests
Async - services communicate with each other using events

#### create an example `Blogs` Project


