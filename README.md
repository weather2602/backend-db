# backend-db

sketch-app-backend-db

Run commands

- create network
  ```sh
  docker network create my-network
  ```
- run container
  ```sh
  docker run -d --network my-network --name mongodb -p 27017:27017 --env-file .env mongo
  ```
