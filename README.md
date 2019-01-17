# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

## Setup Steps

Follow these steps first: https://docs.docker.com/compose/rails/

## Run Locally

```
docker-compose up
```

## Deployments

Build your image:
```
docker-compose build web
```

Push your stuff to docker hub https://hub.docker.com

```
docker login
docker tag rails-demo fadieliya/rails-demo
docker push fadieliya/rails-demo
```

Then deploy to beanstalk, which pulls and runs the built image

```
eb deploy
```

We don't have a default `Dockerfile` in the directory so beanstalk won't try to build it on deploy
