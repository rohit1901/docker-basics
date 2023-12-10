# Basic Docker Operations

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
