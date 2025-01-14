# Infrastructure Repository

This repository orchestrates the deployment of our full-stack application, which includes a Vite.js React frontend and an Express backend with Prisma. The infrastructure setup relies on Docker Compose for container orchestration and Git submodules to integrate the frontend and backend codebases.

## Prerequisites

Before proceeding, please ensure the following tools are installed on your system:
- [Git](https://git-scm.com/)
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

## Setup

### Cloning the Repository

To clone the infrastructure repository and its submodules, execute the following commands in your terminal:

```bash
git clone https://github.com/phybyte/mvx-dapp-infra.git
cd mvx-dapp-infra
```
### Copy .env.local file

```bash
cp .env.local .env
```

### Domain name

Dont forget to change the domain name in the nginx/nginx.conf file to your domain name if you wish to deploy the application on a domain.

## Start

### Docker Compose

To start the entire stack, run the following command:

```bash
docker-compose up -d
```

This will build and start the containers defined in the `docker-compose.yml` file.

## Nginx Configuration

The `nginx` directory contains the `nginx.conf` file used for configuring the Nginx server as a reverse proxy.
