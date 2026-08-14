# Technical Guftgu Static Website

This is a static website for **Technical Guftgu** that showcases training programs, trainer info, and contact details.

## 📁 Project Structure

- `index.html` – Homepage
- `about.html`, `courses.html`, `contact.html` – Additional pages
- `css/style.css` – Styles
- `images/` – Trainer photo and logo

---

## Deployment Instructions (Amazon Linux 2 EC2)

### ✅ Prerequisites

- EC2 instance (Amazon Linux 2)
- Port 80 open in security group
- SSH key and access
- Upload(SCP) Or Clone the Code


## SSH into EC2 and install nginx and deploy website

### Install nginx
```bash
sudo yum update -y
sudo yum install nginx -y
sudo systemctl enable nginx
sudo systemctl start nginx
```
### Deploy WebContent
```bash
# Remove Existing(Already Deployed) Files 
sudo rm -rf /usr/share/nginx/html/*
# Clone or pull(If already Cloned) Latest Code
sudo yum install git -y
git clone https://github.com/technicalguftgu/web-app.git
sudo cp -r web-app/* /usr/share/nginx/html/
```
### start/restart nginx
```bash
sudo systemctl restart nginx
```
### Access Website

Visit:  
```
http://<EC2_PUBLIC_IP>
``
 

---

© 2026 Technical Guftgu
