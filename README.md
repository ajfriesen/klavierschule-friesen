# klavierschule-friesen


Running management commands
As with any shell command that we wish to run in our container, this is done using the docker-compose -f local.yml run command.

To migrate your app and to create a superuser, run:

$ docker-compose -f local.yml run django python manage.py migrate
$ docker-compose -f local.yml run django python manage.py createsuperuser
Here we specify the django container as the location to run our management commands.

## Get into the containers bash

docker exec -it <some-id> bash