# **Labwork** MongoDB, Express, React, NodeJS

> UWS 2020 - Internet Technologies

# Task 1: Plain Express

### Run Project:

- Start Docker Desktop
- `cd express1`
- `docker build -t linushe/mern-demo1 .`
- `docker run -p 49160:8080 -d linushe/mern-demo1`
- Open Files & Console in Docker Container via Remote in VSCode
- Open http://localhost:49160/

### Learning Outcomes

- See HTTP Status via `curl http://localhost:49160`

# Task 2a: Express Application Files

### Run Project:

- Start Docker Desktop
- `cd express_generator`
- `docker build -t dt/express-generator .`
- `docker run --rm -v ${pwd}:/usr/src dt/express-generator express --view=pug -f myapp`

### Learning Outcomes

- How to create a automated file structure
- in bin/www (file) is described how express4 is working

# Task 2b: Build runnable Express App

### Run Project:

- Start Docker Desktop
- `cd express_app1`
- `docker build -t dt/express-development .`
- `docker run --name myapp1 -p 3000:3000 -it dt/express-development`
- Open http://localhost:3000/
- Open Files & Console in Docker Container via Remote in VSCode

### Learning Outcomes
- How to Setup & Run an App using Express, Nodemon & Docker

# Task 3: Restful Server

### Run Project:

- Start Docker Desktop
- `cd express_app2`
- `docker build -t dt/express-rest .`
- `docker run --name myapp2 -p 3000:3000 -it dt/express-rest`
- Open http://localhost:3000/
- Open Files & Console in Docker Container via Remote in VSCode

### mongo Stack
MongoDB
- `docker pull mongo`

MongoDB with Backend Interface
- `docker pull mongo-express`


> Run manually 
- `docker run --name some-mongo -d mongo:tag`

- `docker run --network some-network -e ME_CONFIG_MONGODB_SERVER=some-mongo -p 8081:8081 mongo-express`

> Or Use Docker-Compose 

- `cd mongo1`
- `docker-compose -f stack.yml up`
- shutdown with `docker-compose -f stack.yml down`


- visit http://localhost:8081 for Mongo Express (DB Admin Tool)

### UML Diagrams (for Databases)
- Use VS Code Extension "PlantUML"

# Task 4: Using Mongoose to communicate between express and mongo

### Run
- `cd express_app3`
- `docker build -t dt/express-development .`
- `docker-compose -f stack.yml up`
- visit http://localhost:8081 for Mongo Express (DB Admin Tool)
- visit http://localhost:3000 for React App
- Example Requests: http://localhost:3000/users , http://localhost:3000/catalog/authors , http://localhost:3000/catalog/book/5dc21650ae5da3ca57ebc53d 
- stop with `docker-compose -f stack.yml down`

# Task 5: Setting up Views for Express App

### Run
- `cd express_app4`
### Cleanup from last Task
- `docker build -t dt/express-development .`
- `docker volume prune`

### Run
- `docker-compose -f stack.yml up`
- visit http://localhost:8081 for Mongo Express (DB Admin Tool)
- visit http://localhost:3000 for React App
- stop with `docker-compose -f stack.yml down`

### Learning Outcomes
- How to create a normalized DB in MongoDB
- Connect View with DB via `mongodb://[username:password@]host1[:port1][,...hostN[:portN]][/[database][?o
ptions]]`
- Created Lists of mongoDB Content with pug templates

# Task 6: Database Interactions in Express
> Including Create, Retrieve, Edit & Delete