# Dockerize Your Django Project
[![Build Status](https://travis-ci.com/IamStefin/dockerizing-django.svg?branch=master)](https://travis-ci.com/IamStefin/dockerizing-django)
[![GitHub license](https://img.shields.io/github/license/IamStefin/dockerizing-django)](https://github.com/IamStefin/dockerizing-django/blob/master/LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/IamStefin/dockerizing-django)](https://github.com/IamStefin/dockerizing-django/stargazers)
[![GitHub issues](https://img.shields.io/github/issues/IamStefin/dockerizing-django)](https://github.com/IamStefin/dockerizing-django/issues)

This repo will give you the basic configuration for setting docker for your django project

# Setup

Clone this repository in your working directory

```bash
git clone https://github.com/IamStefin/dockerizing-django.git
```

Place your project in the **MyProject** directory 

Go to `settings.py` and change the `DATABASE` section matching your credentials in `docker-compose.yml`

This project uses `WhiteNoise` to serve static files and `django-probes` for checking database connection

## SSL Certificate for https

Run this command to get your SSL certificate from LetsEncrypt

```bash
certbot run -a manual -i nginx -d example.com
```

Paste your certificate and key in `nginx/ssl/nginx.crt` and `nginx/ssl/nginx.key` respectively. 

## Port Setup

Open port 80 and 443

## Starting the server 

```bash
docker-compose build
docker-compose up -d
```

## Creating superuser

```bash
docker exec -it dockerizing-django_website_1 bash
python manage.py createsuperuser
```

## Contributing

Feel free to make this code better :)

## Contributors

<a href="https://github.com/iamstefin/dockerizing-django/graphs/contributors">
  <img src="https://contributors-img.web.app/image?repo=iamstefin/dockerizing-django" />
</a>
