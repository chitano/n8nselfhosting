# 🚀 n8n Installation on Ubuntu (Docker)

This repository provides step-by-step instructions and configuration files to install **[n8n](https://n8n.io/)** on a Ubuntu Linux server using Docker.  
It is designed for anyone who wants to quickly set up **n8n** for workflow automation with minimal effort.

---

## 📋 Prerequisites

Before starting, make sure you have:

- A Ubuntu 24.04 LTS server 
- Root or sudo access
- A domain/subdomain (e.g. `n8n.example.com`) pointing to your server’s IP  
- (Optional but recommended) An SSL certificate (e.g. via [Let's Encrypt](https://letsencrypt.org/))

---

## ⚙️ Installation Steps

### 0. Install and Preparing Server

```bash
sudo apt update
sudo apt upgrade

```

### 1. Install docker 

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh

```

Now you will have docker installed in your ubuntu server. 

### 2. Clone this Repository

```bash
git clone https://github.com/chitano/n8nselfhosting
cd n8nselfhosting

```

### 3. Change user group 
```bash
sudo usermod -aG docker your_user_name #if you install debian on AWS lightsail it will be "ubuntu"

```
### 4. Create a folder called "local-files"

```bash
mkdir local-files

```
### 5. Change .env file for your own domain

### 6. Pull images and run server.
```bash
sudo docker compose pull
sudo docker compose up -d


