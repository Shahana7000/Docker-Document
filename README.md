# Docker-Document
here would be all the dockers command 
# 🐳 Docker Commands Cheat Sheet

A complete reference of commonly used Docker commands, organized by category with explanations and usage examples.

---

## 1️⃣ Docker Basics

| Command | Description | Example |
|---------|-------------|---------|
| `docker --version` | Check Docker version installed | `docker --version` |
| `docker info` | Display system-wide information about Docker | `docker info` |
| `docker help` | Show help for Docker commands | `docker help` |

---

## 2️⃣ Images

| Command | Description | Example |
|---------|-------------|---------|
| `docker images` | List all local images | `docker images` |
| `docker pull <image>` | Download an image from Docker Hub | `docker pull ubuntu` |
| `docker build -t <name> .` | Build an image from a Dockerfile | `docker build -t myapp .` |
| `docker rmi <image>` | Remove one or more images | `docker rmi ubuntu` |
| `docker tag <src> <repo:tag>` | Tag an image for a repository | `docker tag myapp myrepo/myapp:latest` |
| `docker history <image>` | Show history of an image | `docker history ubuntu` |
| `docker save -o file.tar <image>` | Save image to a tar archive | `docker save -o myimage.tar myapp` |
| `docker load -i file.tar` | Load an image from a tar archive | `docker load -i myimage.tar` |

---

## 3️⃣ Containers

| Command | Description | Example |
|---------|-------------|---------|
| `docker ps` | List running containers | `docker ps` |
| `docker ps -a` | List all containers (including stopped) | `docker ps -a` |
| `docker run <image>` | Create and start a container | `docker run ubuntu` |
| `docker run -it <image> /bin/bash` | Run interactively with a shell | `docker run -it ubuntu /bin/bash` |
| `docker run -d <image>` | Run container in detached mode | `docker run -d nginx` |
| `docker run --name <name> <image>` | Assign a name to container | `docker run --name web nginx` |
| `docker start <container>` | Start a stopped container | `docker start mycontainer` |
| `docker stop <container>` | Stop a running container | `docker stop mycontainer` |
| `docker restart <container>` | Restart a container | `docker restart mycontainer` |
| `docker kill <container>` | Force stop a running container | `docker kill mycontainer` |
| `docker rm <container>` | Remove a container | `docker rm mycontainer` |
| `docker exec -it <container> <cmd>` | Run a command in a running container | `docker exec -it mycontainer /bin/bash` |
| `docker attach <container>` | Attach local terminal to running container | `docker attach mycontainer` |
| `docker logs <container>` | View container logs | `docker logs mycontainer` |
| `docker rename <old> <new>` | Rename a container | `docker rename oldname newname` |
| `docker cp <container>:<src> <dest>` | Copy file from container to host | `docker cp mycontainer:/file.txt .` |
| `docker cp <src> <container>:<dest>` | Copy file from host to container | `docker cp file.txt mycontainer:/` |

---

## 4️⃣ Volumes (Data Persistence)

| Command | Description | Example |
|---------|-------------|---------|
| `docker volume ls` | List all volumes | `docker volume ls` |
| `docker volume create <name>` | Create a volume | `docker volume create mydata` |
| `docker volume inspect <name>` | Show volume details | `docker volume inspect mydata` |
| `docker volume rm <name>` | Remove a volume | `docker volume rm mydata` |
| `docker run -v <volume>:<path> <image>` | Mount volume into container | `docker run -v mydata:/data ubuntu` |

---

## 5️⃣ Networks

| Command | Description | Example |
|---------|-------------|---------|
| `docker network ls` | List networks | `docker network ls` |
| `docker network create <name>` | Create a network | `docker network create mynetwork` |
| `docker network inspect <name>` | Inspect network details | `docker network inspect mynetwork` |
| `docker network connect <net> <container>` | Connect container to network | `docker network connect mynetwork mycontainer` |
| `docker network disconnect <net> <container>` | Disconnect container from network | `docker network disconnect mynetwork mycontainer` |
| `docker network rm <name>` | Remove a network | `docker network rm mynetwork` |

---

## 6️⃣ Docker Compose

| Command | Description | Example |
|---------|-------------|---------|
| `docker compose up` | Start all services in `docker-compose.yml` | `docker compose up` |
| `docker compose up -d` | Start in detached mode | `docker compose up -d` |
| `docker compose down` | Stop and remove services, networks, volumes | `docker compose down` |
| `docker compose ps` | List running services | `docker compose ps` |
| `docker compose logs` | View logs for services | `docker compose logs` |
| `docker compose build` | Build/rebuild services | `docker compose build` |

---

## 7️⃣ System Cleanup

| Command | Description | Example |
|---------|-------------|---------|
| `docker system df` | Show disk usage | `docker system df` |
| `docker system prune` | Remove unused data | `docker system prune` |
| `docker system prune -a` | Remove all unused images, containers, networks | `docker system prune -a` |
| `docker image prune` | Remove unused images | `docker image prune` |
| `docker container prune` | Remove stopped containers | `docker container prune` |
| `docker volume prune` | Remove unused volumes | `docker volume prune` |

---

## 8️⃣ Export / Import Containers

| Command | Description | Example |
|---------|-------------|---------|
| `docker export <container> > file.tar` | Export container’s filesystem as tar | `docker export mycontainer > backup.tar` |
| `docker import file.tar` | Import container from tar file | `docker import backup.tar` |

---

## 9️⃣ Inspecting & Debugging

| Command | Description | Example |
|---------|-------------|---------|
| `docker inspect <object>` | Show details of container/image/network | `docker inspect mycontainer` |
| `docker stats` | Display live container resource usage | `docker stats` |
| `docker top <container>` | Show processes running inside container | `docker top mycontainer` |
| `docker events` | Monitor Docker events in real-time | `docker events` |

---

## 🔟 Docker Hub Login & Push

| Command | Description | Example |
|---------|-------------|---------|
| `docker login` | Log in to Docker Hub | `docker login` |
| `docker logout` | Log out from Docker Hub | `docker logout` |
| `docker push <repo:tag>` | Push image to Docker Hub | `docker push myrepo/myapp:latest` |
| `docker pull <repo:tag>` | Pull image from Docker Hub | `docker pull myrepo/myapp:latest` |

---

## 📌 Notes
- Always tag images with versions to avoid pulling unwanted latest versions.
- Use `-d` (detached mode) for background containers.
- Use `--rm` to auto-remove containers after exit.

---

**Author:** _Your Name_  
**Repository:** `docker-container-command`
