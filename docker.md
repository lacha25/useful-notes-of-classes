# Docker

## Core Concepts

- Image: application template
- Container: running instance of an image
- `Dockerfile`: instructions to build an image
- Volume: persistent data
- Bind mount: host folder mounted into a container
- Network: communication between containers
- Compose: configuration for multi-container applications

## Inspection Commands

- `docker version`
- `docker info`
- `docker ps`
- `docker images`
- `docker volume ls`
- `docker network ls`

## Images

- `docker pull IMAGE[:TAG]`
- `docker build -t NAME[:TAG] PATH`
- `docker image rm IMAGE`

## Containers

- `docker run [OPTIONS] IMAGE [COMMAND] [ARG...]`
- Common options:
  - `-d` detached mode
  - `-it` interactive terminal
  - `--name NAME`
  - `-p HOST:CONTAINER` to map ports
  - `--rm` to remove the container on exit
- Lifecycle commands:
  - `docker start CONTAINER`
  - `docker stop CONTAINER`
  - `docker restart CONTAINER`
  - `docker rm CONTAINER`
  - `docker kill CONTAINER`

## Monitoring and Storage

- `docker logs CONTAINER`
- `docker stats [CONTAINER]`
- `docker volume create [NAME]`
- `docker volume inspect VOLUME`

## Compose

- `docker compose up [-d]`
- `docker compose down`
- `docker compose ps [--all]`
- `docker compose logs`
- `docker compose build [SERVICE]`
