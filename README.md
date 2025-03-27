# backend-db

## Overview

Manages the MongoDB database, storing authentication data for the `auth-service` and image data for the `backend-service` using GridFS.

## Prerequisites

<details><summary><b>Show Prerequisites</b></summary>
  
- Docker (for containerization)
- MongoDB (if running locally without Docker)

</details>

## Commands

<details><summary><b>Show Commands</b></summary>
  
### Setup

- Create the Docker network:
  ```sh
  docker network create my-network
  ```

### Build

- Build the Docker image:
  ```sh
  docker build -t backend-db .
  ```

### Run

- Run the container:
  ```sh
  docker run -d -p 27017:27017 --network my-network --env-file .env backend-db
  ```

### Debugging

- Check logs:
  ```sh
  docker logs <container-id>
  ```

### Environment Variables

- Create a .env file with:
  ```diff
  MONGO_ROOT_USER=admin
  MONGO_ROOT_PASS=admin
  MONGO_INITDB_DATABASE=sketch-app
  ```

</details>
