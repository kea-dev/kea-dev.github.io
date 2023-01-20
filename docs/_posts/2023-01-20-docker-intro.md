---
layout: post
title:  "Docker Intro"
date:   2023-01-20 17:31:17 +0000
categories: docker training
author: lakruzz
---

1. [Purpose](#purpose)
1. [Learning objectives](#learning-objectives)
1. [Structure](#structure)
1. [Questions](./QUESTIONS.md)

---

{% include toc.html html=content %}

---

{% include toc.html html=content sanitize=true class="inline_toc" id="my_toc" h_min=2 h_max=3 %}

---

# Purpose
This module introduces the fundamentals of [[Docker]] 

# Learning objectives
Understand the Docker concepts, Setup Docker environment for personal/development use, build images and run containers

# Structure 

# Questions
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


 