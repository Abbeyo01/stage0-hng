# Static Website Deployment on Azure Virtual Machine (VM)

## Introduction

This project involves deploying a static website on an Azure Vitual Machine (VM) using the NGINX web server. The website includes HTML, CSS, and JavaScript files and contains information about the developer, including their name, username, and email.

## Requirements

- Cloud Platform: Azure VM
- Web Server: NGINX
- Static Website: A ready-to-deploy static website project (HTML, CSS, JavaScript) which includes your Name, username, and email.
- Website Content: Contains a link to HNG Internship.

## Steps to Deploy

### 1. Launch an Azure Virtual Machine

- Log in to your Azure Portal.
- Navigate to the Virtual Machines section.
- Launch a new instance.
  - Choose Ubuntu Server as the operating system.
  - Select an appropriate size (e.g., Standard B1ls).
  - Configure networking:
   - Allow inbound traffic for HTTP (port 80) and SSH (port 22).
- Review and create the virtual machine.
  

### 2. Connect to Your Azure Virtual Machine

- Obtain the public IP address of your Azure VM from the Azure Portal.
- Connect to the VM using SSH:
  
  ssh -i /path/to/your-key.pem azureuser@your-azureuser-public-ip


### 3. Install NGINX

- Update your package lists:

sudo apt update

Install NGINX:

sudo apt install nginx -y


### 4. Configure NGINX

-  Navigate to the default NGINX directory and configure NGINX

cd /var/www/html

Remove the default index.nginx-debian.html file:

sudo rm index.nginx-debian.html


### 5. Upload Your Static Website Files

- Use SCP or any preferred method to transfer your static website files (HTML, CSS, JavaScript) to /var/www/html on your Azure VM:

scp -i /path/to/your-key.pem -r /path/to/your-website-files/* azureuser@your-azureuser-public-ip:/var/www/html


### 6. Update NGINX Configuration

Edit the default NGINX configuration file to ensure it serves your website correctly


### 7. Restart NGINX

Restart the NGINX service to apply the changes






# stage0-hng
