# Wordpress-Docker-Heroku Template

A working, as of 23rd April 2023, and simple WordPress project template for Heroku deployment and local Docker development.

## Deploying to Heroku

Set up a new app on Heroku for your WordPress project. 

Deploying to Heroku requires a connection to an existing MySQL database.

Example
```
WORDPRESS_DB_HOST=database.xxxxxxxxxxxx.eu-west-2.rds.amazonaws.com
WORDPRESS_DB_NAME=wordpress
WORDPRESS_DB_USER=admin
WORDPRESS_DB_PASSWORD=password
```

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/rory-ferguson/wordpress-docker-heroku)

## Local Development

Install Docker [https://www.docker.com/products/docker-desktop/](https://www.docker.com/products/docker-desktop/)

Clone this repository and change directory into `wordpress-docker-heroku`

Create an `.env` file at the root of the directory, with the following environment variables
```
IP=127.0.0.1
WORDPRESS_DB_NAME=wordpress
WORDPRESS_DB_USER=admin
WORDPRESS_DB_PASSWORD=password
```

Run docker 
```
docker-compose up
```

The above is only required to be ran on initial install

Run the start command if the containers/volume already exist.
```
docker-compose start
```

You can now navigate to http://127.0.0.1 to start working with your local WordPress installation.
