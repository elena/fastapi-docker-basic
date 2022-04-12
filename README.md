# Basic FastAPI Docker Setup

Intended to be related to the following fully baked cookiecutter projects:

* https://github.com/tiangolo/full-stack-fastapi-postgresql 
* https://github.com/tiangolo/full-stack-fastapi-couchbase

These stacks are awesome and huge! Thanks [@tiangolo](https://github.com/tiangolo/) for the great work! :sparkleheart:

Sometimes you just need a quick setup. This is intended to provide that setup.

Issues and PRs welcome.

Defaults (details in [Configuration](#configuration) below, please feel free to change these, this is just some values to get going)

* Python version: `python3.8`
* Localhost: http://localhost:8081
* image name: `my-fastapi-image`


## Quickstart

Install docker and have the daemon running: https://docs.docker.com/get-docker/

    $ docker build -t my-fastapi-image .

_Don't forget the `.`_


    $ docker compose up -d

See your FastAPI app running at http://localhost:8081 :tada:


## Configuration

Defaults in this repo. Please change them to suit your needs:

Python version:

    Dockerfile#1: FROM python:3.8

localhost:PORT -- set to `8081`

_Don't need to change the `80`, that's set in the Dockerfile and is only used "internally" by that image._

    docker-compose.yaml#6: "8081:80"


image name `my-fastapi-image`

    $ docker build -t my-fastapi-image .

    docker-compose.yaml#4    image: my-fastapi-image
