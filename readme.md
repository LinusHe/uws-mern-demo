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
- stoppen mit `docker-compose -f stack.yml down`