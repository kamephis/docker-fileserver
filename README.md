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
```

### 2. Create the pub Directory
Make sure to create a pub directory in the root of this project. This directory will contain the files you want to make available through the file server.

```bash
mkdir pub
```
You can now place your files in the pub directory.

### 3. Start the Docker Container
Use Docker Compose to start the NGINX server and mount your pub directory.

```bash
docker-compose up -d
```
This will start the server in detached mode.

### 4. Access the File Server
Once the container is running, you can access your file server in a web browser at:

```bash
http://localhost:8890
```
You will see a directory listing of your files in the pub folder.

### 5. Stop the Server
To stop the server, run:

```bash
docker-compose down
```
This will stop and remove the Docker container.

File Structure
```bash
.
├── docker-compose.yml    # Defines the Docker services and configuration
└── pub/                  # Directory containing the files to be served
```
### Configuration
The pub directory is mounted into the Docker container at /usr/share/nginx/html.
The server listens on localhost:8890.
If you wish to change the port or the directory, you can modify the docker-compose.yml file.

### License
This project is licensed under the MIT License. See the LICENSE file for details.
