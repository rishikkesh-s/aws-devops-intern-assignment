# AWS DevOps Engineer Internship Assignment

## Objective

Deploy a simple static website on an AWS EC2 Ubuntu instance using Nginx and document the deployment process.

## AWS Services Used

* **Amazon EC2** - Created and configured a virtual server to host the website.
* **Security Groups** - Configured inbound rules for SSH (Port 22) and HTTP (Port 80).

## Implementation Steps

### 1. EC2 Instance Setup

* Launched an Ubuntu EC2 instance.
* Configured Security Group rules:

  * SSH: Port 22
  * HTTP: Port 80
* Connected to the instance using SSH.

### 2. Nginx Installation

Updated system packages and installed Nginx:

```bash
sudo apt update
sudo apt install nginx -y
```

Checked Nginx service status:

```bash
sudo systemctl status nginx
```

Verified that Nginx was running on port 80:

```bash
sudo ss -tulpn | grep :80
```

### 3. Website Deployment

Created a custom HTML webpage containing:

* Name
* College
* Branch
* Email
* Current Date

The default Nginx webpage was replaced with the custom webpage located at:

```
/var/www/html/index.html
```

The website was accessed successfully using the EC2 public IP address.

## Linux Commands Used

| Command                     | Purpose                    |
| --------------------------- | -------------------------- |
| `sudo apt update`           | Update package information |
| `sudo apt install nginx -y` | Install Nginx web server   |
| `systemctl status nginx`    | Check Nginx status         |
| `systemctl restart nginx`   | Restart Nginx service      |
| `df -h`                     | Check disk usage           |
| `free -m`                   | Check memory usage         |
| `ps aux`                    | View running processes     |

## Repository Contents

```
├── index.html
├── README.md
└── screenshots/
    ├── EC2_instance.png
    ├── SSH_Login.png
    ├── Nginx-installation.png
    ├── Nginx-status.png
    └── Nginx-website.png
```

## Problems Faced

* Configuring SSH key permissions.
* Connecting to the EC2 instance using the private key.
* Replacing the default Nginx webpage.

## Learnings

* Learned EC2 instance deployment and basic AWS networking.
* Learned Linux server administration commands.
* Learned how to deploy a static website using Nginx.
* Learned GitHub repository management.

## Time Taken

Completed within 1 day as part of the AWS DevOps Engineer Internship Assignment.

