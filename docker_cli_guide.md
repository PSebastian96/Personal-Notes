# Docker CLI Guide for Linux

This guide covers installation, setup, container management, and status checks using Docker CLI on Linux.

---

## 1. Installing Docker on Linux

**Ubuntu / Debian:**
```bash
# Update packages
sudo apt update

# Install prerequisites
sudo apt install -y apt-transport-https ca-certificates curl gnupg lsb-release

# Add Docker’s official GPG key
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

# Add Docker repository
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

# Install Docker Engine
sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

# Start and enable Docker service
sudo systemctl start docker
sudo systemctl enable docker
```

**Verify installation:**
```bash
docker --version
docker run hello-world
```

---

## 2. Common Docker CLI Commands

### 2.1 Docker System / Setup
```bash
docker info
docker version
docker plugin ls
```

### 2.2 Managing Images
```bash
docker images
docker image ls
docker pull ubuntu:22.04
docker rmi <image_id_or_name>
```

### 2.3 Creating & Running Containers
```bash
docker run -it ubuntu:22.04 /bin/bash
docker run -dit --name mycontainer ubuntu:22.04
docker run -dit -p 8080:80 --name webserver nginx
docker run -dit -v /host/path:/container/path --name mycontainer ubuntu:22.04
```
*Flags:*
- `-d` → detached (background)
- `-i` → interactive
- `-t` → allocate a pseudo-TTY
- `--name` → assign a container name
- `-p` → port mapping
- `-v` → volume mapping

### 2.4 Starting / Stopping / Restarting Containers
```bash
docker start mycontainer
docker stop mycontainer
docker restart mycontainer
docker kill mycontainer
docker rm mycontainer
```

### 2.5 Checking Container Status
```bash
docker ps
docker ps -a
docker inspect mycontainer
docker logs mycontainer
docker logs -f mycontainer
```

### 2.6 Executing Commands Inside a Container
```bash
docker exec -it mycontainer /bin/bash
docker exec mycontainer ls /app
```

### 2.7 Networking
```bash
docker network ls
docker network inspect bridge
docker network connect mynetwork mycontainer
docker network disconnect mynetwork mycontainer
```

### 2.8 Volume Management
```bash
docker volume ls
docker volume create myvolume
docker volume rm myvolume
```

### 2.9 Docker Compose (Optional)
```yaml
# docker-compose.yml example
version: '3'
services:
  web:
    image: nginx
    ports:
      - "8080:80"
  db:
    image: mysql
    environment:
      MYSQL_ROOT_PASSWORD: example
```
```bash
docker compose up -d
docker compose down
docker compose logs -f
```

### 2.10 Cleaning Up
```bash
docker container prune
docker image prune
docker volume prune
docker network prune
docker system prune -a
```

---

## 3. Tips for Linux Users
```bash
# Add user to Docker group
sudo usermod -aG docker $USER
newgrp docker

# Monitor container resource usage
docker stats

# Filter containers by status
docker ps -a --filter "status=exited"
```

---

This guide provides a full reference for Docker CLI usage on Linux.

