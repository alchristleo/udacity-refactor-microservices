# Udagram Image Filtering Microservice

Udagram is a simple cloud application developed alongside the Udacity Cloud Engineering Nanodegree. It allows users to register and log into a web client, post photos to the feed, and process photos using an image filtering microservice.

The project is split into three parts:
1. [The Simple Frontend](/udacity-c3-frontend)
A basic Ionic client web application which consumes the RestAPI Backend. 
2. [The RestAPI Feed Backend](/udacity-c3-restapi-feed), a Node-Express feed microservice.
3. [The RestAPI User Backend](/udacity-c3-restapi-user), a Node-Express user microservice.
4. [Deployment template](/udacity-c3-deployment), contains docker and kubernetes yaml config.

## Getting Setup

We will use npm to install all the dependency on each service. 
```sh
cd && touch .profile
** go to root project
sudo cp .config.example ~/.profile
```

Fill all of the key needed, you must have:
- aws account
- aws cli, aws eksctl, aws s3 bucket, aws rds (postgres)
- docker and kubernetes
- travis ci

## Debug locally

Navigate to `udacity-c3-deployment/docker`, then run:
```sh
docker-compose -f docker-compose-build.yaml build --parallel
docker-compose -f docker-compose-build.yaml push
docker-compose up
```
