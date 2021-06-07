Mifos X Credit Scoring Module
============

The project consisted of providing an AI powered solution to the users for credit assessment of loans. The project covered various aspects from classical AI, considering various statistical models, to the modern day neural network. The project is enriched with various credit modeling techniques, giving access to the user to choose one or any from them. It also takes care of the different data sources from which data can be fetched and has been fully incorporated to handle data coming from various sources like JSON/XML or SQL.

It is a RESTFUL API module written in [django](https://www.djangoproject.com/) and [Django Rest framework](https://www.django-rest-framework.org/)


Getting started
============

1. Ensure you have the following installed in your system:

    [`git`](https://git-scm.com/downloads)


Requirements
============
* MySQL v5.7
* python v3.6.8+

You can install python for your platform by following the python getting started [guide](https://wiki.python.org/moin/BeginnersGuide/Download).

Setting up local development environment
============

To set up server locally you need to install all the requirements listed in requirements.txt.
But first, you need to create and activate your project virtual environment by using the commands:
    
    python -m venv env

For Linux or MacOS environment:
    
    source env/bin/activate

For windows environment:

    ./env/bin/activate

You can then install project dependencies using the following command:

    pip install -r requirements.txt

Instructions to to run migrations
============

Once you have successfully installed all the dependencies, you need to run the database migrations.
First, you need to ensure your database connection is properlty configured.
Start by making sure you have the required version of MySQL installed.
Alternatively, you can run the required version of the database server in a container, instead of having to install it, like this:

    docker run --name mysql-5.7 -p 3306:3306 -e MYSQL_ROOT_PASSWORD=mysql -d mysql:5.7

and stop and destroy it like this:

    docker rm -f mysql-5.7

Beware that this database container database keeps its state inside the container and not on the host filesystem.  It is lost when you destroy (rm) this container.  This is typically fine for development.  See [Caveats: Where to Store Data on the database container documentation](https://hub.docker.com/_/mysql) re. how to make it persistent instead of ephemeral.

You can the run the required project migrations using the command:

    python manage.py migrate

Instructions to run application
============

Start the application server by running the command:

    python manage.py serve

The app will start at http://127.0.0.1:8000/

- You can access DRF browsable API at: http://127.0.0.1:8000/api/
- You can access swagger docs at: http://127.0.0.1:8000/api/docs/swagger-ui
- You can access redoc docs at: http://127.0.0.1:8000/api/docs/redoc

Instructions to configure IDE
============

For vscode(Visual Studio Code) users, you can follow this [guide](https://code.visualstudio.com/docs/python/tutorial-django) to setup your ide for django project development

## Want to help? [![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/openMF/web-app/issues)

Want to file a bug, request a feature, contribute some code, or improve documentation? Excellent! Read up on our guidelines for [contributing](.github/CONTRIBUTING.md) and then check out one of our [issues](https://github.com/openMF/web-app/issues). Make sure you follow the guidelines before sending a contribution!
