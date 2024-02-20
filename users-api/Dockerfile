FROM maven:3.6.3-jdk-8-slim AS building

WORKDIR /home/microservice-app-example/users-api
COPY . /home/microservice-app-example/users-api

RUN mvn clean package

FROM openjdk:8-jdk-alpine

EXPOSE 8083

COPY --from=building /home/microservice-app-example/users-api/target/users-api-0.0.1-SNAPSHOT.jar  users-api-0.0.1-SNAPSHOT.jar
ENTRYPOINT ["sh","-c","java -jar users-api-0.0.1-SNAPSHOT.jar"]
