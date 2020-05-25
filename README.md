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
```
  181  cd Documents/CODEBASE/Microservices/
  182  mkdir blog
  183  cd blog
  184  npx create-react-app client
  185  mkdir posts
  186  cd posts/
  187  npm init -y
  188  npm i express cors axios nodemon
  189  cd ..
  190  ls
  191  mkdir comments
  192. cd comments
  192  npm init -y
  193  npm i axios cors express nodemon
  ```
  
