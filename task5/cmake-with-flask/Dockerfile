FROM gcc:latest

WORKDIR /opt/techprog

COPY . .

RUN apt-get update && apt-get install -y build-essential cmake

RUN cmake . && make



FROM python:3.8-slim-buster

WORKDIR /opt/techprog

COPY . .

RUN apt-get update -y
RUN apt-get install -y python-pip python-dev build-essential

#RUN pip install -r requirements.txt

ENTRYPOINT ['python']

CMD ['app.py']

RUN useradd -d /opt/techprog tp2022user

USER tp2022user