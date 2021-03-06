# FDK Translations API

## Description

FDK Translations API allows managing translations documents used in various FDK application.

## Installation and Usage

- Required tools to run this project:
  - Node.js and npm to run locally on a host machine
  - Docker and Docker Compose to run locally in a container

#### Running application locally on a host machine

- Install dependencies by running `npm install`
- Run one of the following commands:
  - `npm start` to start local development server
  - `npm run debug` to start local development server in debug mode

#### Running application in a Docker container

- Build a Docker container using the following command:
  - `docker build -t fdk-translations-api .`
- Run the container using the following comand:
  - `docker run -d -p 8080:8080 -e NODE_ENV -e HOST -e PORT -e PLAYGROUND -e INTROSPECTION fdk-translations-api`

#### Running application using Docker Compose

- Run the application using the following command:
  - `docker-compose up -d`

## Environment Variables

- `NODE_ENV` - current environment
  - `development`
  - `production`
- `HOST` - application hostname (optional)
  - `0.0.0.0` (default)
- `PORT` - application port (optional)
  - `8080` (default)
- `PLAYGROUND` - makes GraphQL Playground available at root URL
  - `true`
  - `false`
- `INTROSPECTION` - enables or disables introspection query
  - `true`
  - `false`

## Contributing

#### Branching Strategy

Whenever a new change is to be implemented, follow these steps:

- Create a new branch from the master branch
- Implement and commit changes
- Create a pull request for code review

#### Commits

This repository uses conventional commmit format. In order to commit, follow these steps:

- Stage files to be committed
- Run `npm run commit` script

Do not use `--no-verify` flag when making commits.

