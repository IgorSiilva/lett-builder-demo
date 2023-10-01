# Node JS Template Repo


## Contributing
- For pattern suggestions or new dev packages, you must open an pull request.

![image](https://user-images.githubusercontent.com/25425920/210374548-90a74608-592a-4ab9-972b-a391e3c6d9c7.png)


## Index

- [Install](#install)
- [Prerequisites](#prerequisites)
- [Running](#running)

## Prerequisites

- [Node.JS (>= {PUT_YOUR_NODE_VERSION_HERE}) and NPM](https://nodejs.org/en/)
- [Docker](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Install

1. Install project dependencies with

```bash
$ npm install
```

2. Configure environment variables. Create a new file named `.env` and copy and paste content of `.env.example` to him, then fill the empty values

## Running

We strongly recommend running this project using Docker.

```bash
# development using Docker
$ start:local:docker (or press F5)
```

## Test

```bash
# unit tests
$ npm run test

# test coverage
$ npm run test:cov
```

## Scripts

```
# Pull image from ECR and run on your docker machine for debugging purposes.
$ aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 868884350453.dkr.ecr.us-east-1.amazonaws.com
$ docker-compose -f docker-compose.${stage}.yml up


# Rebuild local image on vscode
1. Press ctrl+shift+p
2. Search for Run Task
3. Run task build-local-docker
```
