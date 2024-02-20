FROM golang:alpine AS build

WORKDIR /home/microservice-app-example/auth-api
COPY . /home/microservice-app-example/auth-api

ENV GO111MODULE=on
RUN go mod init github.com/bortizf/microservice-app-example/tree/master/auth-api
RUN go clean -modcache

RUN go mod tidy

EXPOSE 8000

RUN go build -v -o /usr/local/bin/auth-api .

CMD [ "auth-api" ]
