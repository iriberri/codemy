# Related Command

## Build the images:
  $ docker-compose -f docker-compose-dev.yml build

## Run the containers:
  $ docker-compose -f docker-compose-dev.yml up -d

## Create the database:
  $ docker-compose -f docker-compose-dev.yml \
    run users-service python manage.py recreate_db

## Seed the database:
  $ docker-compose -f docker-compose-dev.yml \
    run users-service python manage.py seed_db

## Run the tests:
  $ docker-compose -f docker-compose-dev.yml \
    run users-service python manage.py test

## To stop the containers:
  $ docker-compose -f docker-compose-dev.yml stop

## To bring down the containers:
  $ docker-compose -f docker-compose-dev.yml down

## Want to force a build?
  $ docker-compose -f docker-compose-dev.yml build --no-cache

## Remove images:
  $ docker rmi $(docker images -q)

## Access postgres:
  $ docker exec -ti users-db psql -U postgres -W \
  $ \c users_dev \
  $ select * from users;

# Microservices with Docker, Flask, and React

[![Build Status](https://travis-ci.org/Desmonddai583/codemy.svg?branch=master)](https://travis-ci.org/Desmonddai583/codemy)