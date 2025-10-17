# HNG13 Stage 0 DevOps Challenge - NGINX Deployment

**Status:** PASS (20/20)

**Name:** Oghenetejiri Edwin
**Slack Username:** @Oghenetejiri

**Live Server IP:** http://34.229.153.75/

---

## Project Overview

This project successfully completed the HNG Stage 0 task by deploying a publicly accessible NGINX web server on **AWS EC2** running **Amazon Linux 2023**. The key challenge was aligning the server's configuration with the exact grading requirements.

### Key Achievements:
* Web server deployed using **NGINX**.
* Custom `index.html` created with the required date format (**DD/MM/YYYY**).
* Publicly accessible on the default **HTTP Port 80**.
* File path successfully configured to the challenge requirement: `/var/www/html/`.

---

## 1. AWS EC2 Instance Provisioning

The setup used an **Amazon Linux 2023 AMI**.

* **Security Group:** Inbound traffic was allowed on **TCP Port 80** from `0.0.0.0/0`.
* **Connection:** Management was handled via **EC2 Instance Connect**.

---

## 2. Server Deployment Steps (Amazon Linux 2023)

The following commands were run via the terminal to set up the server:

### A. Install and Start NGINX
Installation was adapted for Amazon Linux's `yum` package manager.

```bash
# Update and install NGINX using amazon-linux-extras
sudo yum update -y
sudo amazon-linux-extras install nginx1 -y

# Start and enable the NGINX service
sudo systemctl start nginx
sudo systemctl enable nginx
