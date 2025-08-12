
# 🚀Complete Guide: Node.js Deployment on Jenkins Using Freestyle Projects 
## Complete Guide: Node.js Deployment on Jenkins Using Freestyle Projects
Automating your Node.js application deployment with Jenkins helps you deliver updates quickly, reliably, and consistently. This tutorial will walk you through setting up Jenkins freestyle projects to pull your code from GitHub, install dependencies, and deploy your Node.js app using PM2.

---
## Prerequisites
- Before you start, make sure you have the following in place:

- A Linux server (Ubuntu/Debian recommended) with Jenkins installed and running. Jenkins runs as a dedicated user (jenkins).

- Jenkins user has sudo privileges so it can install software and manage processes.

- Git plugin installed in Jenkins (usually pre-installed).

- Node.js application source code hosted on a Git repository (e.g., GitHub).

- Open Jenkins web UI port (default 8080) accessible via your firewall/security groups.

- Open your Node.js application port (e.g., 3000) in firewall/security group to allow external access.

---
### System Setup: Installing Node.js and PM2 for Jenkins User
#### 1. Switch to the Jenkins User
Jenkins jobs run under the jenkins user account. You need to install Node.js and PM2 as this user:
```
sudo su - jenkins
```
#### 2. Update Package Lists
Always start by updating your package lists:
```
sudo apt update
```
### 3. Add Node.js LTS Repository
Add the Node.js LTS repository maintained by NodeSource:
```
sudo curl -fsSL https://deb.nodesource.com/setup_lts.x | bash -
```
### 4. Install Node.js
Install Node.js and npm from the added repository:
```
sudo apt-get update
sudo apt install -y nodejs
```



