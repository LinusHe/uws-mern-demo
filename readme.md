# **Labwork** MongoDB, Express, React, NodeJS

> Labsheets by Derek Turner

> © UWS 2020 - Internet Technologies

> Based on: https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs

# Task 1: Plain Express

> PDF: [Labsheet 1](https://github.com/LinusHe/uws-mern-demo/blob/master/labsheets/nodeexpress1.pdf)

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

> PDF: [Labsheet 2](https://github.com/LinusHe/uws-mern-demo/blob/master/labsheets/nodeexpress2.pdf)

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

> PDF: [Labsheet 3](https://github.com/LinusHe/uws-mern-demo/blob/master/labsheets/nodeexpress3.pdf)

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

> PDF: [Labsheet 4](https://github.com/LinusHe/uws-mern-demo/blob/master/labsheets/nodeexpress4.pdf)

### Run
- `cd express_app3`
- `docker build -t dt/express-development .`
- `docker-compose -f stack.yml up`
- visit http://localhost:8081 for Mongo Express (DB Admin Tool)
- visit http://localhost:3000 for React App
- Example Requests: http://localhost:3000/users , http://localhost:3000/catalog/authors , http://localhost:3000/catalog/book/5dc21650ae5da3ca57ebc53d 
- stop with `docker-compose -f stack.yml down`

# Task 5: Setting up Views for Express App

> PDF: [Labsheet 5](https://github.com/LinusHe/uws-mern-demo/blob/master/labsheets/nodeexpress5.pdf)

### Cleanup from last Task
- `docker build -t dt/express-development .`
- `docker volume prune`

### Run
- `cd express_app4`
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

> PDF: [Labsheet 6](https://github.com/LinusHe/uws-mern-demo/blob/master/labsheets/nodeexpress6.pdf)

> Including Create, Retrieve, Edit & Delete

### Cleanup from last Task
- `docker build -t dt/express-development .`
- `docker volume prune`
### Run
- `cd express_app5`
- `docker-compose -f stack.yml up`
- visit http://localhost:8081 for Mongo Express (DB Admin Tool)
- visit http://localhost:3000 for React App
- stop with `docker-compose -f stack.yml down`

### Learning Outcomes
- Create Detail Views (Genre, Book, Author, Instance): e.g. http://localhost:3000/catalog/genre/5dd32a734a04a9aecd2829b1
- Create Forms (new Genres, Authors, Books, Instances): e.g. http://localhost:3000/catalog/genre/create
- Delete Forms (Author) - Other Delete Forms are not implemented yet!
- Update Forms (Book) - Other Update Forms are not implemented yet!

# Todos:
- implement Delete & Update Forms