FROM node:12
ENV DEBUG="myapp:*"

# Create app directory
RUN mkdir -p /usr/src/app
COPY ./myapp/package.json /usr/src/app/package.json
WORKDIR /usr/src/app
RUN npm install && mv /usr/src/app/node_modules /node_modules ;\
  npm install -g nodemon

COPY ./myapp /usr/src/app

VOLUME ["/usr/src/app"]
EXPOSE 3000
CMD [ "npm","run","start" ]
