FROM python:3.6-alpine
WORKDIR /home/microservice-app-example/log-message-processor
COPY . /home/microservice-app-example/log-message-processor

RUN apk add --no-cache build-base
RUN pip3 install -r requirements.txt

CMD ["python3","-u","main.py"]
