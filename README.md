# Enhancing Deployment: Automating 3-Tier Architecture with Ansible & Docker

## Description

In this project, I aimed to enhance deployment efficiency by automating a 3-tier application architecture using Ansible and Docker. The goal was to create a reproducible and scalable environment that simplifies the deployment process. The architecture consists of a presentation tier, an application logic tier, and a data storage tier, each encapsulated in Docker containers for isolation and ease of management. Ansible played a pivotal role in automating the provisioning and orchestration of these containers, ensuring consistent deployments. Throughout the project, I tackled various challenges, such as ensuring seamless communication between containers and maintaining configuration consistency. The outcome was a significant reduction in deployment time and an increase in system reliability, demonstrating the power of combining Ansible’s automation capabilities with Docker’s containerization benefits.

## Steps to Set Up the Project

### 1. Setup AWS EC2 Instances

- **Two AWS EC2 instances:**
  - One instance will be the Ansible master node.
  - One instance will be the Ansible slave node.

- **Add the slave node to the Ansible inventory file**: `/etc/ansible/hosts`

### 2. Download the Docker Collection in Ansible Master Node

```bash
ansible-galaxy collection install community.docker
```

### 3. Install Docker and Start Docker Services
- Create the `install_docker.yml` Ansible playbook:
- Run the playbook:

```bash
ansible-playbook install_docker.yml
```

### 4. Launch the Web Server Container
- Create the `web_server.yml` Ansible playbook:
- Run the playbook:

```bash
ansible-playbook web_server.yml
```

### 5. Setting Up MySQL and WordPress Containers
- Create the `word_sql.yml` Ansible playbook:
- Run the playbook:

```bash
ansible-playbook word_sql.yml
```

##Conclusion
This project demonstrated the effectiveness of using Ansible and Docker to automate the deployment of a 3-tier architecture. By leveraging Ansible's automation capabilities and Docker's containerization benefits, we achieved a reproducible and scalable deployment environment, significantly reducing deployment time and increasing system reliability.

##Contact
If anything is not working or needs changes, connect with me on [LinkedIn](https://www.linkedin.com/in/mrphiloo/).

