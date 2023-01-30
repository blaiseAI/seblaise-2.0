---
title: "Setting up a Dockerized NestJS App with PostgreSQL and Prisma ORM"
date: 2023-01-30T13:27:00+07:00
slug:
category: snippets
summary:
description:
cover:
  image: "covers/docker-posgres-prisma"
  alt: "docker-posgres-prisma"
  caption:
  relative: true
showtoc: true
draft: false
---

## Snippet Purpose

As a developer, I often encounter challenges while setting up a new NestJS application with Docker and PostgreSQL. Despite being a crucial step in the development process, this task can be time-consuming and prone to errors. To streamline this process, I have created this guide to simplify the setup of a Dockerized NestJS app with PostgreSQL and Prisma ORM. This guide is designed to save time and minimize the chances of running into common issues, making it an essential resource for anyone looking to quickly and efficiently set up a NestJS application with Docker and PostgreSQL.

> Note: These snippets assume you have a NestJS application and Docker installed. For NestJS setup, refer to: https://docs.nestjs.com/first-steps. For Docker installation, see: https://docs.docker.com/get-docker/. Enjoy using these snippets to set up your Dockerized NestJS app with PostgreSQL and Prisma ORM.

## Create a PostgreSQL instance

You will be using PostgreSQL as the database for your NestJS application. This tutorial will show you how to install and run PostgreSQL on your machine through a Docker container.

First, create a `docker-compose.yml` file in the main folder of your project:

```
touch docker-compose.yml
```

This `docker-compose.yml` file is a configuration file that will contain the specifications for running a docker container with PostgreSQL setup inside. Create the following configuration inside the file:

```
# docker-compose.yml

version: '3.8'
services:
  dev-db:
    image: postgres:13
    ports:
      - 5434:5432
    environment:
      POSTGRES_USER: postgres
      POSTGRES_PASSWORD: 123456
      POSTGRES_DB: nest
    networks:
      - networkName
networks:
  networkName:

```

Make sure that nothing is running on port `5434` of your machine. To start the postgres container, open a new terminal window and run the following command in the main folder of your project:

```
docker-compose up  dev-db -d
```

Congratulations 🎉. You now have your own PostgreSQL database!

## Set up Prisma

Now that the database is ready, it's time to set up Prisma!

## Initialize Prisma

To get started, first install the Prisma CLI as a development dependency. The Prisma CLI will allow you to run various commands and interact with your project.

```
npm install -D prisma
```

You can initialize Prisma inside your project by running:

```
npx prisma init
```

This will create a new prisma directory with a schema.prisma file. This is the main configuration file that contains your database schema. This command also creates a .env file inside your project.

## Set your environment variable

Inside the .env file, you should see a DATABASE_URL environment variable with a dummy connection string. Replace this connection string with the one for your PostgreSQL instance.

```
// .env
DATABASE_URL="postgresql://postgres:123456@localhost:5434/nest?schema=public"
```

Congratulation 🎉. This concludes the final step of Setting up a Dockerized NestJS App with PostgreSQL and Prisma ORM

Learn more about prisma ORM, see: https://www.prisma.io
