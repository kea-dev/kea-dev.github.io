---
layout: post
title:  "Technology Intro"
categories: technology training
author: lakruzz
published: false
---
Technology is a topic and a discipline just like _system development_ and _programming_. We will utilize tech and tech stacks to sustain and automate other disciplines, including _collaboration_, _documentation_, _verification_. The technology topic will focus on _infrastructe as code_ well actually _anything as code_.
{: .kicker}

# Structure
This module is developed in the context of AP programme for Computer Science at Copenhagen School of Technology and Design (KEA). It's part of the fulfillment of the curriculum of the topic [_technology_](https://katalog.kea.dk/course/3050241/2022-2023){: target="_blank"}.



# Learning objectives
You will get to know the concepts Docker is built on; what it is, where it comes from, how it works, what it's used for and where it's headed. 

You will know how to setup Docker on you own PC as well as a few other ways to gain access to docker in your environment. 

You will get to use and build images and run containers.

You will familiarise yourself with the Docker <em title="Command Line Interface">CLI</em> and you will practice the most basic commands as well as the most basis syntax of the `Dockerfile`.

You will become a Docker practitioner - a prerequsite to bear titles sucs as _Fullstack Developer_ and _DevOps Enginieer_.


## Basics

- What is Docker?
- What is the relation between a _Docker image_ and a _Docker container._
- What is a `Dockerfile`.
- How is Docker installed on _Windows_, _Mac._ 
- What is [Docker Hub](https://dockerhub.com).
- What does the following commands do? (demonstrate, and elborate on the most useful options and arguments.)
  - `docker build [OPTIONS] PATH | URL | -`
  - `docker ps [OPTIONS]`
  - `docker rm [OPTIONS] CONTAINER [CONTAINER...]`
  - `docker rmi [OPTIONS] IMAGE [IMAGE...]`
  - `docker run [OPTIONS] IMAGE [COMMAND] [ARG...]`
  - `docker exec [OPTIONS] CONTAINER COMMAND [ARG...]`
  - `docker images [OPTIONS] [REPOSITORY[:TAG]]`
- Explain the [syntax](https://docs.docker.com/engine/reference/builder/) of a `Dockerfile` including:
  - `FROM`
  - `CMD`
  - `RUN`
  - `COPY`
  - `ENTRYPOINT`

## Advanced
- How is _Docker_ different from a _Virtual Machine?_
- How can _Docker_ become available on non-linux OS (e.g. _Windows_ and _MacOS_)?
- How is Docker installed on _Ubuntu (Debian)._
- What does the following commands do? (demonstrate in a terminal and elborate the most useful options and arguments.)
  - `docker push [OPTIONS] NAME[:TAG]`
  - `docker image COMMAND`
  - `docker buildx [OPTIONS] COMMAND`
- Explain the [syntax](https://docs.docker.com/engine/reference/builder/) of a `Dockerfile` including:
  - `ADD`
  - `EXPOSE`
  - `LABEL`
  - `WORKDIR`
  - `VOLUME`
- Explain how to install a Docker CLI extension use? [pushrm](https://github.com/christian-korneck/docker-pushrm) as an example.


 

# Questions