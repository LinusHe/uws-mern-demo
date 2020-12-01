# **Labwork** MongoDB, Express, React, NodeJS

> UWS 2020 - Internet Technologies


# Task 1: Plain Express 

### Run Project: 
* Start Docker Desktop
* `cd express1`
* `docker build -t linushe/mern-demo1 .`
* `docker run -p 49160:8080 -d linushe/mern-demo1`
* Open Files & Console in Docker Container via Remote in VSCode
* Open http://localhost:49160/

### Learning Outcomes
* See HTTP Status via `curl http://localhost:49160`

# Task 2a: Express Application Files

### Run Project: 
* Start Docker Desktop
* `cd express_generator`
* `docker build -t dt/express-generator .`
* `docker run --rm -v ${pwd}:/usr/src dt/express-generator express --view=pug -f myapp`

### Learning Outcomes
* How to create a automated file structure
* in bin/www (file) is described how express4 is working

