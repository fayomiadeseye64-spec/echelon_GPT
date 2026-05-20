# 🤖 Echelon GPT – Enterprise AI Chat Application Deployment

## 📌 Overview

Echelon GPT is a scalable AI-powered web application built with Streamlit, LangChain, and OpenAI.

The project was upgraded from a lightweight local application into a production-style cloud architecture deployed on Amazon Web Services (AWS), designed to support increasing traffic and scalability demands.

The infrastructure now supports automatic scaling up to **25 EC2 CentOS instances**, enabling high availability, fault tolerance, secure HTTPS communication, and global content delivery using CloudFront.

This project demonstrates practical cloud engineering, AI application deployment, Linux server administration, scalability implementation, and enterprise AWS architecture design.

---

# 🧠 Project Objective

- Deploy a scalable AI chat application on AWS
- Host Streamlit applications on CentOS EC2 servers
- Implement enterprise-grade cloud architecture
- Enable secure HTTPS communication using AWS ACM
- Improve global performance using Amazon CloudFront
- Configure automatic scaling and high availability
- Demonstrate production-ready AI application deployment workflow

---

# ✨ Features

- 🧠 GPT-powered conversational AI
- 🌐 Interactive Streamlit web interface
- 🔐 Secure OpenAI API key handling
- 🎈 Dynamic UI elements and animations
- 🖼️ AI-themed user interface
- ☁️ Enterprise AWS cloud deployment
- 📈 Auto Scaling infrastructure
- 🌍 Global delivery using CloudFront CDN
- 🔒 HTTPS enabled using ACM SSL certificates

---

# ⚙️ Technologies Used

## AI & Application Stack
- Python
- Streamlit
- LangChain
- OpenAI API

## Cloud Platform
- Amazon Web Services (AWS)

## Compute & Scalability
- EC2 (Elastic Compute Cloud)
- Auto Scaling Group (ASG)
- Application Load Balancer (ALB)

## Security & Networking
- IAM (Identity and Access Management)
- VPC
- Security Groups
- AWS Certificate Manager (ACM)

## Content Delivery
- Amazon CloudFront
- Amazon S3

## Operating System
- CentOS Linux

---

# 📁 Project Structure

```bash
echelon_GPT/
│
├── app.py                # Main Streamlit application
├── requirements.txt      # Python dependencies
├── ai.png                # UI image asset
└── README.md             # Project documentation
```

---

# 🏗️ Enterprise Architecture Overview

The application architecture was redesigned into a scalable cloud-native infrastructure capable of handling increasing user traffic efficiently.

## Architecture Flow

User  
↓  
CloudFront CDN  
↓  
Application Load Balancer (ALB)  
↓  
Auto Scaling Group (Up to 25 CentOS EC2 Instances)  
↓  
Streamlit Application  
↓  
OpenAI API

---

# ☁️ AWS Services Implemented

## ✅ Amazon EC2
Used to host the Streamlit AI application on CentOS Linux servers.

## ✅ Auto Scaling Group (ASG)
Automatically scales infrastructure from 1 server up to 25 EC2 instances depending on traffic demand and health monitoring.

## ✅ Application Load Balancer (ALB)
Distributes incoming traffic across multiple application servers for high availability and performance optimization.

## ✅ Amazon CloudFront
Configured as a Content Delivery Network (CDN) to improve application speed, reduce latency, and deliver content globally.

## ✅ AWS Certificate Manager (ACM)
Used to provision SSL/TLS certificates for secure HTTPS communication.

## ✅ Amazon S3
Used for static assets, backups, and deployment storage.

## ✅ IAM
Configured for secure access control and permission management.

---

# 🔐 Security Features

- HTTPS enabled using ACM SSL certificates
- Secure traffic delivery through CloudFront
- IAM roles used instead of hardcoded credentials
- SSH access restricted to trusted IP addresses
- Security Groups configured with least privilege access
- API key input secured through password field
- Only required ports exposed publicly

---

# 🚀 Deployment Steps

## 1️⃣ Launch EC2 CentOS Instances

Deploy CentOS EC2 instances within an Auto Scaling Group.

### Required Security Group Rules

| Port | Protocol | Purpose |
|------|----------|----------|
| 22 | TCP | SSH Access |
| 80 | TCP | HTTP |
| 443 | TCP | HTTPS |
| 8501 | TCP | Streamlit Application |

---

## 2️⃣ Connect to EC2 via SSH

### SSH Command

```bash
ssh -i your-key.pem centos@<EC2-PUBLIC-IP>
```

---

## 3️⃣ Update the CentOS Server

```bash
sudo yum update -y
```

---

## 4️⃣ Install Python & Git

```bash
sudo yum install python3 git -y
```

---

## 5️⃣ Clone the Repository

```bash
git clone https://github.com/fayomiadeseye64-spec/echelon_GPT.git

cd echelon_GPT
```

---

## 6️⃣ Create Virtual Environment

```bash
python3 -m venv venv
```

---

## 7️⃣ Activate Virtual Environment

### Linux / CentOS

```bash
source venv/bin/activate
```

---

## 8️⃣ Install Project Dependencies

```bash
pip install -r requirements.txt
```

---

## 9️⃣ Run the Streamlit Application

```bash
streamlit run app.py --server.port 8501 --server.address 0.0.0.0
```

---

# 🌍 Accessing the Application

## Direct EC2 Access

```bash
http://<EC2-PUBLIC-IP>:8501
```

## Production Access Through CloudFront + HTTPS

```bash
https://your-domain-name.com
```

---

# 🌍 CloudFront Configuration

Amazon CloudFront was configured to:

- Improve global application performance
- Reduce latency worldwide
- Cache static assets
- Increase scalability
- Improve user experience
- Add additional security layer

CloudFront distribution was connected to the Application Load Balancer as the origin.

---

# 🔒 SSL/HTTPS Configuration with ACM

AWS Certificate Manager (ACM) was implemented to:

- Generate and manage SSL/TLS certificates
- Enable secure HTTPS communication
- Protect user traffic and API requests
- Integrate securely with CloudFront and ALB

---

# 📈 Scalability Design

The infrastructure supports:

- Automatic horizontal scaling
- Up to 25 EC2 application instances
- High availability deployment
- Fault tolerance
- Traffic distribution using ALB
- Automatic health checks and recovery

This architecture ensures the application remains stable and responsive during high traffic periods.

---

# 🧪 How It Works

1. User enters an OpenAI API key securely
2. User submits a prompt through the Streamlit UI
3. LangChain processes the request
4. OpenAI generates a response
5. Response is displayed in real-time

---

# 🖼️ UI Features

The application interface includes:

- Sidebar API key input
- AI image support (`ai.png`)
- Dynamic placeholders
- Interactive animations 🎈
- Clean and responsive Streamlit UI

---

# 📸 Screenshots (To Add)

- Streamlit application UI
- EC2 instances dashboard
- Auto Scaling Group configuration
- Application Load Balancer
- CloudFront distribution
- ACM SSL certificate
- HTTPS application access
- AWS Architecture Diagram

---

# 🛠️ Future Improvements

- Add Amazon RDS database integration
- Implement CI/CD using GitHub Actions
- Add Docker containerization
- Deploy with Kubernetes using Amazon EKS
- Add monitoring using CloudWatch
- Configure Route 53 DNS management
- Add AWS WAF for enhanced security
- Implement Infrastructure as Code using Terraform

---

# 📜 License

This project is open-source.

You may add an MIT License for public distribution and collaboration.

---

# 👤 Author

**Fayomi Adeseye**  
Cloud Solution Architect (Junior)

## 🔗 GitHub

https://github.com/fayomiadeseye64-spec

---

# ⭐ Project Value

This project demonstrates:

- AI application deployment on AWS
- Enterprise cloud architecture design
- Linux server administration using CentOS
- Streamlit production deployment
- Auto Scaling implementation
- Load balancing configuration
- CloudFront CDN integration
- HTTPS implementation using ACM
- Secure OpenAI API integration
- Production-ready cloud engineering workflow

---

# 📬 Contact

Feel free to connect for collaboration, cloud engineering opportunities, or AI infrastructure discussions.
