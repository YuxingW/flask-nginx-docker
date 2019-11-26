# flask-nginx-docker
Docker template for hosting Flask and Nginx on docker on separated containers.

This repo created because it was always time consuming to `Dockerize` a Python app and nginx with docker. With this repo you are able to run your web application on containers.

## Good to know
You can change the ip addresses of the Nginx easily in the `docker-compose.yml`:

```
version: '3.1'
services:
    web-server:
        build:
            context: ./nginx
            dockerfile: Dockerfile
        ports:
            - 5001:80
            - 5002:443
```

I used ports `5001` and `5002` in case `80` and `443` have been consumed already.

## Work To Do

1. Add certbot docker conatiner to nginx for automatically issues certificate from LetsEncrypted.


## PS
I'm a big fan of [Digital Ocean](https://m.do.co/c/adaf50520737), my wife and I had an application we wanted to host it on [Digital Ocean droplets](https://m.do.co/c/adaf50520737), to make things easier for us we preferred to deploy that app with Docker.
