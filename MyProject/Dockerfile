FROM python:latest

MAINTAINER Stef sstefin@bk.ru

COPY requirements.txt /app/

WORKDIR ./app

RUN pip install -r requirements.txt

EXPOSE 8000

CMD gunicorn MyProject.wsgi -b :8000