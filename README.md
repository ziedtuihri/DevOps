# Docker_tutorial
<img src="./Images/Screenshot_20211225_205904.png "/>



# Docker Commands Reference

## 🐳 Docker Images

```bash
# List non-dangling images (default behavior) with a valid tag and repository 🔍  
sudo docker images

# List all images, including intermediate ones without tag and repository 🔍  
sudo docker images -a

# Remove dangling images (cleanup)  ❌
sudo docker image prune

# Show all running containers ⚓
sudo docker ps

# Show all containers (running and stopped) ⚓
sudo docker ps -a

# Show all volumes 🔍  
sudo docker volume ls

# Remove all Voume  ❌
docker volume prune
```
## 🤖 Jenkins

```bash 
# 🔄 Restart Jenkins  
sudo service jenkins restart  
# Restarts the Jenkins service to apply changes or resolve issues.  

# ⛔ Stop Jenkins  
sudo service jenkins stop  
# Stops the Jenkins service completely.  

# ▶️ Start Jenkins  
sudo service jenkins start  
# Starts the Jenkins service if it's not running.  

# 📊 Check Jenkins Status  
sudo service jenkins status  
# Displays whether Jenkins is active, stopped, or experiencing issues.
```
