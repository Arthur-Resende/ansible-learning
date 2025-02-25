# 🛠️ Ansible Learning

## 📖 Overview

This project was built so I could review essential Ansible and Linux concepts before taking on new tasks involving them at work. In it, there'll be a Docker Compose setup for the demonstration of an Ansible environment, Ansible playbooks, and inventories, as well as a simple static website to be deployed in one of the playbooks. 🌐

## ⚙️ Setup Instructions

### ✅ Prerequisites

Ensure you have the following installed on your system:
- Docker & Docker Compose
- Git

### 🚀 Steps

1. **Clone the repository**

   ```sh
   git clone https://github.com/your-repo/ansible-docker-project.git
   cd ansible-docker-project
   ```

2. **Start Docker Containers**

   ```sh
   docker-compose up -d
   ```

3. **Copy your SSH key to the control node**

   ```sh
   # Generate them if necessary
   ssh-keygen -t rsa -f ~/.ssh/id_rsa -N ""
   ssh-copy-id -p 2201 ansible@localhost
   ```

4. **Access the Ansible Control Node**

   ```sh
   ssh -p 2201 ansible@localhost
   ```

5. **Run Playbooks**

   ```sh
   ansible-playbook playbooks/install_nginx.yml
   ansible-playbook playbooks/deploy_website.yml
   ansible-playbook playbooks/manage_memory.yml
   ansible-playbook playbooks/manage_cpu.yml
   ```

## 📂 Project Structure

```
ansible-docker-project/
│── docker-compose.yml
│── inventory.ini
│── ansible.cfg
│── inventories/
│   ├── inventory.ini
│   ├── inventory.yaml
│── playbooks/
│   ├── install_nginx.yml
│   ├── deploy_website.yml
│   ├── deploy_website/
│   │   ├── config_nginx.yml
│   │   ├── download_webpage.yml 
│   │   ├── extract_webpage.yml
│── inventories/
│   │── inventory.yaml
│   │── inventory.ini
│── README.md
```
