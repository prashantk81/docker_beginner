# docker_beginner

### Docker File -> Docker image -> Docker container

Creating docker file is not mandatory all the time, sometime you can take directly images but if you are creating custom application, you can take any base image and add on some instructions in a docker file.

## Steps

- Create a Dockerfile
- Add instructions in Dockerfile to create Docker image
- Run Dockerfile to create Docker image
- Run Docker image to create Docker container
- Access the application running in Docker container

## Commands

- To check docker is running or not `docker info`
  If it is not then `sudo service docker start`
- After creating docker file `docker build .`
  if you want to tag that image with some name use `docker build -t myapp .`
- Check docker images `docker images`
- Run docker container from the image `docker run -p 8080:80 myapp`
  tells docker to run the myapp container and map port 8080 on your local machine to port 80 inside the container

Using this command, the container is created and running and you are inside the container, you can not do any other actions. You have to run the container in a detached mode

- Run in a detached mode `docker run -d -p 8080:80 myapp`
- To check container's list `docker ps`
- Access the app `http://localhost:8080`
- Stop a container `docker stop container_id`
- Remove a image `docker rmi imageName or id`

## push on docker hub

- `docker login`
- tag the image `docker tag image_name:latest prashant81/repo_name:latest`
- push the image `docker push prashant81/my_first_repo:latest`
