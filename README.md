# Course of Docker with commands
### Docker with Postgres

`Source of docker apps`:https://hub.docker.com/
`Source of docker documentation`:https://docs.docker.com/

![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/9acc6f57-574f-45d0-af71-3b89f573e131)# docker-course
1. `docker pull postgres` Docker will download the latest version of the PostgreSQL image to your local system.
2. `docker run -e POSTGRES_PASSWORD=mysecretpassword postgres`will start a PostgreSQL container using the "postgres" image from Docker Hub.
   ![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/c41f2a11-ef4d-47b4-a100-c3df8bd1d72f)
~ Below is an image of my container after starting the postgres, the image is from the docker desktop apps.
3. ` docker run -e POSTGRES_PASSWORD=mysecretpassword -d postgres` - `-d`: This flag stands for "detached mode." It runs the container in the background (detached) rather than blocking the terminal with container logs. This is useful for running containers that don't require direct interaction with the terminal.
![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/6b7bdafc-0524-4e33-a0eb-a9625bef4a0e)
4. `docker ps`:  command is used to list the currently running containers on your system.
![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/cc8530b3-0606-43b9-8b8c-09eabaecae4f)
![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/acd6a682-8745-42a9-9143-c1cc8beadd44)

5. `docker run --name postgres-latest -e POSTGRES_PASSWORD=mysecretpassword -d postgres` - the command to create a PostgreSQL container named `"postgres-latest"` with the specified environment variables. The container will be running in the background with the provided environment variables, including the `POSTGRES_PASSWORD` set to `mysecretpassword`.
![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/ecc2a59d-7c08-4d2e-b0ba-92e660467201)
![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/857241d0-3059-4b5f-baf4-37fb549fb45a)
6. Display images
   ![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/1ac5f27c-3e54-4752-a94c-9adaec6fad47)
7. `docker exec -it postgres-latest bash` - Access the PostgreSQL container's shell using `docker exec`:
![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/0ac6125b-1479-4a9c-8c9c-3f81e89a6a14)
8. Stop containers by using `id` or `container name`:
   ![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/99dab347-4e18-43ff-b1c3-17d91001881f)
   ![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/1479dbdd-2bab-46e3-b0b6-6a93f16014fc)
9. Start docker by using `id` or `container name`
    ![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/a57eb700-125d-4a9e-8abc-a685ac0a7c89)

10. `docker container prune` - will permanently delete all stopped containers, so make sure you have backups or don't need any data from them before proceeding.
    ![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/a3969f92-7112-41dd-a45f-3405c70003d0)

- Stopped containers:
![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/29276937-44df-4090-b787-6a29f26d81f3)

- after pruning 
    ![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/c8991b0b-9c20-4aa8-bda8-56fe5330c4d2)
- No container:
  ![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/6ce0ac49-c946-4aeb-b9de-fe9467a51e08)

11. `docker volume ls` - To list all volumes on your system, you can use:
    ![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/324acc7f-8ca6-4fe7-a266-0cc1a7c6bb7b)


# Docker Mongodb
1. `docker pull mong` - download the latest version of mongodb to the local machine
2. `docker image ls` - list all images from my containers
3. ` docker run --name my-mongo-one -d mongo` - create and run mongodb with specified name 

![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/0237ef5b-493a-4951-8c3b-dcbd4bbad3ba)
![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/916ae77a-3394-4bca-a9fb-24bc23db7fe6)
4. `docker run --name my-mongodb -p 4000:27017 mongo` - change the default port to 4000 port number of mongodb
![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/fc1bc2aa-8604-4079-aff7-45110bcce79f)
5. ` docker run --name my-mongodb-one -p 4000:27017 -d mongo` - i can use detache as well 
![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/f629014b-5772-4ff6-8ad8-cad76e4a4cb8)
![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/7524a39c-3118-42c1-85b2-cb970f3abd19)
![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/2d0d6f2d-2687-4bee-bd97-0bdb372e2c96)
![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/3bd7fc0e-326d-4232-bd8a-297aea86728d)

## docker mongo-express
1. `docker network create mongo-network` - create a network named "mongo-network":
2. `docker run -p 27017:27017 -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin -e ME_CONFIG_MONGODB_ADMINPASSWORD=password --name mongodb --net mongo-network -d mongo
` - run the MongoDB container with the corrected command
![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/c7963eb5-6ecf-47e9-b925-7eada81cf2c5)
![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/c901bc6c-e50b-40bc-b84c-5e2915bba8a2)
![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/a9cd2d15-2c11-4fc5-bff8-2c1c2f6a3abc)


3. `docker network ls` - list all networks
4. ![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/7a939b73-b948-4c30-8aa3-0b370a4463a1)
5. To create a Docker container named "mongodb" with MongoDB using the following command:

```bash
docker run \
   -p 27017:27017 \
   -e MONGO_INITDB_ROOT_USERNAME=admin \
   -e MONGO_INITDB_ROOT_PASSWORD=password \
   --name mongodb \
   --net mongo-network \
   -d mongo
```
   ![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/4a431465-361a-482b-ae56-15015a31936c)
![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/47c0324f-9cc4-41a3-8bcd-71bbbf37f226)

```
 docker run \
-d -p 8081:8081 \
-e ME_CONFIG_MONGODB_ADMINUSERNAME=admin \
-e ME_CONFIG_MONGODB_ADMINPASSWORD=password \
-e ME_CONFIG_MONGODB_SERVER=mongodb \
--net mongo-network \
--name mongo-exprexpress \
mongo-express
``` - The provided command creates a Docker container named "mongo-exprexpress" based on the "mongo-express" image.
![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/84f759f3-4804-4c3c-8d19-57d23e1e52fc)

```
Our `"mongo-exprexpress"` container is now running and accessible through `http://localhost:8081` or `http://<your_host_ip>:8081` in a web browser, allowing you to interact with MongoDB using the `"mongo-express"` web-based interface.
```
![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/7d557db1-e81d-4614-9402-6b739cc6289a)

`The container running in the browser` -- This is how we are connected to the mongodb 
![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/39f6823d-b897-4dd5-9ce3-508da9e17161)

**`Note:`** If the database is not running the container stop as well.












