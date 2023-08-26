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








