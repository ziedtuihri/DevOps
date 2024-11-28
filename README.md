# Docker_tutorial
<img src="./Images/Screenshot_20211225_205904.png "/>



# Docker Commands Reference

## 🐳 Docker Images

```bash
# List non-dangling images (default behavior) with a valid tag and repository
sudo docker images

# List all images, including intermediate ones
sudo docker images -a

# Remove dangling images (cleanup)
sudo docker image prune

## 📦 Docker container

# Show all running containers
sudo docker ps

# Show all containers (running and stopped)
sudo docker ps -a
