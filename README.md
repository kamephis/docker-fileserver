# Docker File Server

This project sets up a simple file server using NGINX in a Docker container. A local directory (`pub`) is mounted into the container and served over HTTP, allowing you to access your files via a browser at `http://localhost:8890`.

## Prerequisites

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started

### 1. Clone the Repository

First, clone this repository to your local machine:

```bash
git clone https://github.com/kamephis/docker-fileserver.git
cd docker-fileserver
