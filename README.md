# Django Starter ButterCMS

Django starter project using ButterCMS. The project uses the sample content that is automatically created when you
create your free trial account on ButterCMS.

[![Built with Cookiecutter Django](https://img.shields.io/badge/built%20with-Cookiecutter%20Django-ff69b4.svg?logo=cookiecutter)](https://github.com/pydanny/cookiecutter-django/)

## Deploy for free

First, clone this repository.

Then click one of the following: 

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

[![Open in Cloud Shell][shell_img]][shell_link]

[shell_img]: http://gstatic.com/cloudssh/images/open-btn.png
[shell_link]: https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/failedguidedog/django-starter-buttercms/tree/deploy-with-gcp&page=editor&open_in_editor=README.md

## Installation

First prepare a virtual environment

```bash
$ python -m venv venv
$ source venv/bin/activate
```

Then install the project requirements

```bash
$ pip install -r requirements/local.txt
```

### API Token

For Django to be able to fetch your ButterCMS content properly, you need to add your API token as an environment variable.
To do that, copy `sample.env` and edit it, so that includes [your API token](https://buttercms.com/join/).

```bash
$ cp sample.env .env
```

```
# .env
BUTTERCMS_API_TOKEN=<Your API Token>
```

### Run the local server

All that's left is running the migrations and running Django's development server

```bash
$ python manage.py migrate
$ python manage.py runserver
```

## Django Settings

Moved to [settings](http://cookiecutter-django.readthedocs.io/en/latest/settings.html).
