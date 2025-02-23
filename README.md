# Ansible Learning Project

## Overview

This project was build so I could review essential ansible and linux concepts before taking new tasks involving them at work. In it there'll be a docker compose to setup the demonstration for ansible environment, ansible playbooks and inventories, as well as a simple static website to be deployed in one of the playbooks.

## Setup Instructions

### Prerequisites

Ensure you have the following installed on your system:
- Docker & Docker Compose
- Git

### Steps

1. **Clone the repository:**

```sh
git clone https://github.com/your-repo/ansible-docker-project.git
cd ansible-docker-project
```

2. **Start Docker Containers:**

```sh
docker-compose up -d
```

3. **Access the Ansible Control Node:**

```sh
docker exec -it ansible_control bash
```

4. **Run Playbooks:**

```sh
ansible-playbook playbooks/install_nginx.yml
ansible-playbook playbooks/deploy_website.yml
ansible-playbook playbooks/manage_memory.yml
ansible-playbook playbooks/manage_cpu.yml
```

## Project Structure

```
ansible-docker-project/
│── docker-compose.yml
│── inventory.ini
│── ansible.cfg
│── playbooks/
│   ├── install_nginx.yml
│   ├── deploy_website.yml
│   ├── manage_memory.yml
│   ├── manage_cpu.yml
│── static-site/
│── README.md
```