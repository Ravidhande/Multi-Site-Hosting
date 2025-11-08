# 🌐 Hosting Multiple Static Websites on a Single EC2 Instance (Amazon Linux 2)

## 🧭 Overview
This project demonstrates how to **host multiple static websites on a single EC2 instance** using **Apache (httpd)** and **port mapping** on **Amazon Linux 2**.  
Each website runs on a different port and serves files from its own directory under `/var/www/`.

---

## 🧱 Architecture
- **Amazon EC2 (Amazon Linux 2)** – Cloud compute instance to host the websites  
- **Apache (httpd)** – Web server configured for multiple virtual hosts  
- **Static Websites** – HTML, CSS, and JS files hosted in separate directories  
- **Port Mapping** – Used to access each site via unique port numbers (8081, 8082, 8083)  
- **GitHub** – For project documentation and version control  

---

## ⚙️ Setup Steps

### 1️⃣ Launch EC2 Instance
- **AMI:** Amazon Linux 2 (Free Tier)
- **Ports Opened:**  
  - 22 (SSH)  
  - 80 (HTTP)  
  - 8081, 8082, 8083 (Custom TCP for websites)

### 2️⃣ Install Apache
```bash
sudo yum update -y
sudo yum install httpd -y
sudo systemctl enable httpd
sudo systemctl start httpd
