# Docker_tutorial
<img src="./Images/Screenshot_20211225_205904.png "/>



# Docker Commands Reference

## 🐳 Docker Images

```bash
# we can add permissions to docker to not repeat any time sudo like this:
sudo chmod 777 /var/run/docker.sock

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
# http://<<IP-VM>>:8080/
# Directory Structure:   /var/lib/jenkins/workspace


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


Finding the IP Address of a Virtual Machine (VM)
To find the IP address of your virtual machine (VM), you can use one of the following two commands:

ip addr
ifconfig

Example:
Here is an example of the output you might see:

Using ip addr:

```bash
Copy code
ens33: 
    inet 192.168.24.129/24 scope global ens33
    valid_lft forever preferred_lft forever
```

Using ifconfig:

```bash
Copy code
ens33: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 192.168.24.129  netmask 255.255.255.0  broadcast 192.168.24.255
        inet6 fe80::20c:29ff:fe02:3905  prefixlen 64  scopeid 0x20<link>
        ether 00:0c:29:02:39:05  txqueuelen 1000  (Ethernet)
```

Ubuntu commande 

<h2>open a folder with grafical interface</h2>

```bash
nautilus /path/to/your/folder
```

<h2> Using a GUI Text Editor: </h2>

gedit (GNOME's default editor):

```bash
Copy code
gedit yourfile.xml
kate (KDE text editor):
```

```bash
Copy code
kate yourfile.xml
mousepad (Lightweight editor for XFCE):
```

```bash
Copy code
mousepad yourfile.xml
```
# Unit Test

check this course :<br>
https://openclassrooms.com/fr/courses/6100311-testez-votre-code-java-pour-realiser-des-applications-de-qualite/6440136-ecrivez-votre-premier-test-junit-avec-le-tdd
# SonarQube Integration with Jenkins  

docs:
https://www.youtube.com/watch?v=9cebihBfF4A
https://github.com/pritisuryawanshi

## What is SonarQube?  
SonarQube is an open-source platform for continuous code quality inspection. It performs static code analysis to identify:  
- **Bugs**  
- **Security vulnerabilities**  
- **Code smells**  

SonarQube helps developers maintain high-quality, secure, and maintainable software by integrating seamlessly into the development workflow. This allows teams to catch issues early and ensure better overall software quality.  

---

## Why Integrate SonarQube with Jenkins Pipeline?  
Integrating SonarQube with Jenkins Pipeline automates the process of continuous code quality and security checks during the CI/CD pipeline.  

### Key Benefits:  
- **Automated Analysis**: Every code change is analyzed automatically for issues like bugs and security vulnerabilities.  
- **Early Feedback**: Developers receive immediate feedback, enabling quick fixes for potential problems.  
- **Enforces Standards**: Ensures that coding standards are followed across the project.  
- **Improved Software Quality**: Consistent checks lead to better quality, maintainability, and security of the software.  

---

## Overview of the Integration  
The integration between SonarQube and Jenkins simplifies static code analysis by automating the process as part of the Jenkins Pipeline. This ensures:  
- **Code is analyzed on every build.**  
- **Issues are flagged early in the development cycle.**  
- **Development teams can focus on delivering high-quality software.**  

# SonarQube Cheat Sheet  

## 1. Installation  
- **Download**: Obtain the SonarQube server from the [official website](https://www.sonarsource.com/).  
- **Extract**: Unzip the downloaded file to a desired location.  
- **Configure**: Modify the `sonar.properties` file to customize the server settings.  
- **Start**: Launch the SonarQube server using the appropriate script or command.  

---

## 2. Integration with CI/CD Pipeline  
- **Install Plugin**: Add the SonarScanner plugin to your CI/CD tool (e.g., Jenkins, Azure DevOps).  
- **Configure Plugin**: Set up the plugin to connect to your SonarQube server.  
- **Add Analysis Step**: Include a SonarQube analysis step in your pipeline configuration file.  
- **Run Pipeline**: Execute the pipeline to trigger the SonarQube analysis.  

---

## 3. Quality Gates  
- **Define Gates**: Set thresholds for code quality metrics such as:  
  - Code coverage  
  - Code duplication  
  - Code smells  
- **Configure in SonarQube**: Create and manage quality gates on the SonarQube server.  
- **Enforce Gates**: Use SonarScanner to validate the code against the quality gates.  
- **Action on Failure**: Fail the build or take corrective measures if thresholds are not met.  

---

## 4. Code Analysis  
- **Key Features**: SonarQube provides detailed insights, including:  
  - Code smells, bugs, vulnerabilities, and security hotspots  
  - Metrics for code coverage, duplication, and technical debt  
- **Multi-language Support**: Analyze code written in various programming languages and frameworks.  

---

## 5. Custom Rules  
- **Define Rules**: Create custom coding standards or import external rule sets.  
- **Configure in SonarQube**: Add custom rules using the rule engine or by importing files.  
- **Run Analysis**: Ensure custom rules are enforced during SonarQube scans.  

---

## 6. Reporting and Notifications  
- **Reports**:  
  - Access detailed code quality reports through the SonarQube web interface.  
  - Export reports in formats such as PDF or XML.  
- **Notifications**:  
  - Set up alerts for quality issues via email, Slack, or other communication channels.  

---

## 7. Plugin Ecosystem  
- **Explore Plugins**: Extend SonarQube’s capabilities with a wide range of plugins.  
- **Popular Plugins**:  
  - SonarLint for IDE integration  
  - SCM plugins for Git or SVN  
  - Issue tracker integrations like JIRA  
- **Install Plugins**: Add functionality for additional languages, integrations, and tools.  

---

## 8. Best Practices  
- **Frequent Analysis**: Run SonarQube scans regularly as part of your CI/CD pipeline.  
- **Set Realistic Gates**: Define thresholds based on project-specific requirements.  
- **Prompt Fixes**: Address issues immediately to reduce technical debt.  
- **Continuous Improvement**: Monitor and improve code quality using reports and metrics.  

---

> **Note**: This cheat sheet offers a concise overview. For detailed instructions and advanced use cases, refer to the [official SonarQube documentation](https://docs.sonarqube.org/).  

