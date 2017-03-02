# docker-drupal

Setup and run Drupal with Docker with Nginx, Percona, and PHP-FPM.

# WIP

This repository is currently not finished, but is currently a work in progress. Settings files need to use environment variables, and some other updates specific to Docker need to take place. Use at your own risk.

## Download Drupal

You can download and install Drupal with Composer by running:

```
docker-compose run --rm setup
```

This will create a new Composer project using the `drupal-composer/drupal-project` repository. This will download files to `/srv/www` within your Docker container, which will also be mounted to the host local directory `./www`.

## Start the web server

You can boot off Nginx by running the following command:

```
docker-composer up -d web
```

You can then visit your web browser to install & configure Drupal by going to `http://localhost:8000`.

## Install configuration

During install, you will want to choose MySQL, and enter the following info for it:

```
Host: mysql
Table: drupal
Username: drupal
Password: drupal
```
