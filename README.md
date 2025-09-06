# 🚀 n8n Installation on Debian (Docker)

This repository provides step-by-step instructions and configuration files to install **[n8n](https://n8n.io/)** on a Debian Linux server using Docker.  
It is designed for anyone who wants to quickly set up **n8n** for workflow automation with minimal effort.

---

## 📋 Prerequisites

Before starting, make sure you have:

- A Debian 11/12 server 
- Root or sudo access
- A domain/subdomain (e.g. `n8n.example.com`) pointing to your server’s IP  
- (Optional but recommended) An SSL certificate (e.g. via [Let's Encrypt](https://letsencrypt.org/))

---

## ⚙️ Installation Steps


### 1. Install docker 

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh ./get-docker.sh --dry-run

Now your will have docker installed in your debian server. 

```

### 2. Clone this Repository

```bash
git clone https://github.com/chitano/n8nselfhosting
cd n8nselfhosting

```

### 3. Change user group 
```bash
sudo usermod -aG docker your_user_name #if you install debian on AWS lightsail it will be "admin"

```

### 4. Pull images and run server.
```bash
docker compose pull
docker compose up -d


