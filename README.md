#Course of Docker with commands
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

6. `docker exec -it postgres-latest bash` - Access the PostgreSQL container's shell using `docker exec`:
![image](https://github.com/ericmaniraguha/docker-course/assets/44385819/0ac6125b-1479-4a9c-8c9c-3f81e89a6a14)

