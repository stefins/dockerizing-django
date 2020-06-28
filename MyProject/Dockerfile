FROM python:latest

MAINTAINER Stef sstefin@bk.ru

COPY requirements.txt /app/

WORKDIR ./app/

RUN pip install --upgrade pip

RUN pip install -r requirements.txt

COPY . .

EXPOSE 8001
