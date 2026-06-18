# 🌐 Nginx Reverse Proxy & SSL Setup Guide

This guide covers the step-by-step process to configure Nginx as a reverse proxy on an Ubuntu/Debian VPS and secure your domain using Certbot (Let's Encrypt) via Snap.

---

## 🛠️ Phase 1: Tool Installation

| Description | Command |
| :--- | :--- |
| Update the local package index to ensure you install the latest software versions available. | `sudo apt update` |
| Install the Nginx web server package to handle incoming traffic and routing. | `sudo apt install nginx -y` |
| Install and update the core environment for Snap, the recommended package manager for Certbot. | `sudo snap install core; sudo snap refresh core` |
| Install Certbot in classic mode to automatically manage and renew SSL certificates. | `sudo snap install --classic certbot` |
| Create a symbolic link to ensure the `certbot` command can be executed globally from any terminal path. | `sudo ln -s /snap/bin/certbot /usr/bin/certbot` |

---

## ⚙️ Phase 2: Nginx Site Configuration

| Description | Command |
| :--- | :--- |
| Open the text editor to create the base configuration file for your domain (defining port 80 blocks). | `sudo nano /etc/nginx/sites-available/your_domain.com` |
| Link the configuration file to the "enabled" sites directory to instruct Nginx to start using it. | `sudo ln -s /etc/nginx/sites-available/your_domain.com /etc/nginx/sites-enabled/` |
| Test the Nginx configuration files for any syntax errors or broken paths before applying changes. | `sudo nginx -t` |
| Restart the Nginx service to apply and activate the new domain configuration. | `sudo systemctl restart nginx` |

---

## 🔒 Phase 3: SSL Certificate Generation (HTTPS)

> ⚠️ **Note:** Ensure you have already created an **A Record** in your DNS settings pointing your domain to the VPS IP address before running this step.

| Description | Command |
| :--- | :--- |
| Launch the interactive Certbot process to validate your domain, download SSL certificates, and auto-configure HTTPS on port 443. | `sudo certbot --nginx -d your_domain.com` |

---

## 🔄 Phase 4: Maintenance

| Description | Command |
| :--- | :--- |
| Perform a dry run simulation to verify that the background automated SSL renewal tasks work properly. | `sudo certbot renew --dry-run` |
