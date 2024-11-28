# Docker_tutorial
<img src="./Images/Screenshot_20211225_205904.png "/>

sudo docker images

sudo docker images -a

sudo docker image prune

sudo docker ps

sudo docker ps -a

# Docker Commands Reference

## 🐳 Docker Images

```bash
# List non-dangling images (default behavior)
sudo docker images

# List all images, including intermediate ones
sudo docker images -a

# Remove dangling images (cleanup)
sudo docker image prune

# Show all running containers
sudo docker ps

# Show all containers (running and stopped)
sudo docker ps -a
