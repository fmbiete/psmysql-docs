# Overview

Percona Server for MySQL is a freely available, fully compatible, enhanced, and open source drop-in replacement for any MySQL database. Percona Server provides superior and optimized performance, greater scalability and availability, enhanced backups, increased visibility, and instrumentation. 

Docker lets developers build, deploy, run, update, and manage containers, which isolate applications from the host system. Docker containers are made from Docker images, which are snapshots of the configuration needed to run an application, such as the code and libraries.

??? Information "Reasons for deploying Percona Server in Docker"

    Deploying a Percona Server for MySQL container is an efficient, fast solution to setting up a database quickly without using too many resources. This type of deployment works best for small to medium applications.

    You should deploy a Percona Server for MySQL database in Docker for several reasons. Here are some of them:

    - Portability: Docker containers can run on any platform that supports Docker. This flexibility lets you move your database or installation steps from one platform to another.
    - Isolation: Docker containers are isolated from each other and the host system. This isolation means you can run multiple instances of MySQL on the same machine without interfering with each other or affecting the host's performance. You can also isolate your database from other applications or services that might pose a security risk or consume too many resources.
    - Scalability: Depending on the load and demand, you can scale docker containers up or down. You can use tools like Docker Compose or Kubernetes to orchestrate multiple containers and manage their configuration, networking, and deployment. You can also use Docker Swarm or Amazon ECS to distribute your containers across multiple nodes and achieve high availability and fault tolerance.
    - Versioning: Docker images and containers contain all the dependencies and configurations needed to run your application. You can use tags to specify different versions of your images and easily switch between them. You can also use Docker Hub or other registries to store and share your images with others.
    - Development: Docker containers can help you create a consistent and reproducible development environment that matches your production environment. You can use tools like Dockerfile or Docker Build to automate the creation of your images and ensure they have the same settings and packages as your production images. You can also use tools like Docker Volumes or Bind Mounts to persist and share your data between containers or the host system.

## Purpose of the Quickstart

This document provides the basic commands and queries to create and run a Percona Server for MySQL database in a Docker container. You are welcome to name any items to match your organization's standards or use your table structure and data. If you do, the results are different from the expected results.

For this document, container refers to the Docker container and instance refers to the database server in the container.

## Prerequisites

[Install Docker](https://docs.docker.com/get-docker/) on your system.

## Steps for first-time users

The following steps guide you through the key processes for a developer. 

- Step 1 [Start and connect to a Docker container](quickstart-docker.md)
- Step 2 [Create a database and table](quickstart-database.md)
- Step 3 [Run queries](quickstart-queries.md)
- Step 4 [Clean up](quickstart-exit.md)
- Step 5 [Choose your next steps](quickstart-next-steps.md)

## Next step

[Start and connect to a Docker container :material-arrow-right:](quickstart-docker.md){.md-button}
