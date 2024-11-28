# Ansible EC2 Apache WebServer Deployment

## 🚀 Overview
This Ansible project automates the deployment and configuration of Apache web servers on Amazon EC2 instances. It sets up multiple web servers with custom HTML content and proper security configurations.

## 📋 Features
- Automated Apache installation and configuration
- Secure passwordless sudo setup
- Custom HTML deployment with dynamic hostname display
- Multi-server deployment support
- Automated service management

## 🏗️ Project Structure
Ansible_EC2_Apache_WebServer/
├── site.yml # Main playbook
├── ansible.cfg # Ansible configuration
├── inventory # Server inventory file
└── test.pem # AWS EC2 key pair (not included in repo)

## 🔧 Prerequisites
- Ansible installed on control machine
- Valid AWS EC2 instances
- SSH access to EC2 instances
- Python installed on target hosts
- AWS EC2 key pair (`.pem` file)

## ⚙️ Configuration
### Inventory Setup
```ini
[webservers]
ec2-54-242-222-126.compute-1.amazonaws.com
ec2-54-144-126-100.compute-1.amazonaws.com
```

##Ansible Configuration(ansible.cfg)
```
[defaults]
inventory = ./inventory
remote_user = ec2-user
private_key_file = ./test.pem
```

## 📘 Usage

### Step 1: Clone the Repository
```bash
git clone https://github.com/yourusername/Ansible_EC2_Apache_WebServer.git
cd Ansible_EC2_Apache_WebServer
```
### Step 2: Update the inventory file with your EC2 hostnames/IPs
### Step 3: Place Your EC2 Key Pair File
### Step 4: Run the Playbook
```bash
ansible-playbook site.yml
```



