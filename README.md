# Basic Docker Operations [![My Skills](https://skillicons.dev/icons?i=docker)](https://skillicons.dev)

This README provides a guide to perform basic Docker operations using commonly used commands.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Commands](#commands)
  - [1. Images](#1-images)
  - [2. Containers](#2-containers)
  - [3. Docker Compose](#3-docker-compose)
- [Additional Resources](#additional-resources)

## Installation

To use Docker, you need to install Docker Engine on your machine. Visit the [Docker website](https://docs.docker.com/get-docker/) for installation instructions based on your operating system.

## Usage

- Ensure Docker is running.
- Open a terminal or command prompt to execute Docker commands.

## Commands

### 1. Images

#### Pull an Image
```bash
docker pull <image_name>
```
Pulls an image from a registry (like Docker Hub).

#### List Images
```bash
docker images
```
Lists all locally available Docker images.

#### Remove an Image
```bash
docker rmi <image_id or image_name>
```
Deletes a specific Docker image from the local machine.

### 2. Containers

#### Run a Container
```bash
docker run <options> <image_name>
```
Creates and starts a container from an image.

#### List Containers
```bash
docker ps
```
Lists all running containers.

#### Stop a Container
```bash
docker stop <container_id or container_name>
```
Stops a running container.

#### Remove a Container
```bash
docker rm <container_id or container_name>
```
Deletes a specific container.

#### Execute Commands in a Running Container
```bash
docker exec -it <container_id or container_name> <command>
```
Runs a command inside a running container.

### 3. Docker Compose

#### Build and Run Services
```bash
docker-compose up
```
Builds and starts all services defined in a `docker-compose.yml` file.

#### Stop Services
```bash
docker-compose down
```
Stops and removes containers, networks, volumes, and images created by `docker-compose up`.

## Additional Resources

- [Docker Documentation](https://docs.docker.com/)
- [Docker Hub](https://hub.docker.com/)
- [Docker Compose Documentation](https://docs.docker.com/compose/)

# Practice Exercises 
Here's a set of basic Docker practice tasks:

### 1. Pulling and Running an Image

- **Task**: Pull an image from Docker Hub and run a container based on that image.
- **Steps**:
    1. Use `docker pull` to fetch an image (e.g., `docker pull nginx` for the Nginx web server).
    2. Run a container using `docker run` with appropriate options (e.g., `docker run -d -p 8080:80 nginx` to start an Nginx container on port 8080).

### 2. Creating Your Own Dockerfile

- **Task**: Create a simple Dockerfile to build a custom image.
- **Steps**:
    1. Create a directory for your Dockerfile and add a basic text file or a simple script.
    2. Write a Dockerfile specifying instructions to build the image.
    3. Use `docker build -t <image_name>:<tag>` to build the image (e.g., `docker build -t my-image:1.0 .`).

### 3. Working with Containers

- **Task**: Create, start, stop, and remove containers.
- **Steps**:
    1. Use `docker run` to start a container.
    2. List running containers using `docker ps`.
    3. Stop a running container with `docker stop <container_id or container_name>`.
    4. Remove a stopped container using `docker rm <container_id or container_name>`.

### 4. Using Volumes

- **Task**: Mount a volume to persist data between the host and the container.
- **Steps**:
    1. Create a directory on your host machine (e.g., `/path/to/host/data`).
    2. Use `-v` flag with `docker run` to mount this directory to a directory inside the container (e.g., `docker run -v /path/to/host/data:/data <image_name>`).

### 5. Docker Compose

- **Task**: Define a multi-container application with Docker Compose.
- **Steps**:
    1. Create a `docker-compose.yml` file defining services, networks, and volumes.
    2. Define at least two services (e.g., a web server and a database).
    3. Use `docker-compose up` to start the application.

### 6. Inspecting Containers and Images

- **Task**: Explore detailed information about containers and images.
- **Steps**:
    1. Use `docker inspect <container_id or image_name>` to get detailed information.
    2. Understand the metadata and configurations stored for containers and images.

### 7. Cleaning Up

- **Task**: Manage unused resources to free up space.
- **Steps**:
    1. Use `docker system prune` to remove all stopped containers, dangling images, and unused networks.
    2. Manually delete specific unused containers, images, or volumes using `docker rm`, `docker rmi`, or `docker volume rm`.
