Docker for PHP with Varnish and Nginx

[![Build Status](https://travis-ci.org/itscaro/docker-php-varnish.svg?branch=master)](https://travis-ci.org/itscaro/docker-php-varnish)

http://localhost:80 - Varnish

http://localhost:81 - Nginx

Getting started

Download composer executable

$ docker run -ti --rm --volume=$(pwd):/scripts php:alpine /scripts/docker/composer-install.sh

$ docker run -ti --rm --volume=$(pwd):/scripts -w /scripts php:alpine /scripts/composer create-project symfony/framework-standard-edition my_project_name

Change in docker-composer.yml, line '.:/workspace' into './my_project_name:/workspace'

$ docker-composer up

You can download symfony executable

$ docker run -ti --rm --volume=$(pwd):/scripts php:alpine  php -r "copy('https://symfony.com/installer', '/scripts/symfony');"

