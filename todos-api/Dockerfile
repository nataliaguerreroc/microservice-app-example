FROM node:8.17.0-alpine

WORKDIR /home/microservice-app-example/todos-api
COPY . /home/microservice-app-example/todos-api

RUN npm install

EXPOSE 8082

CMD ["npm","start"]
