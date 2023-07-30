
# Deploying Docker application using Ansible Playbook

This Ansible project automates the configuration and deployment of an httpd (Apache) server using Docker. 

## Prerequisites

Before running the Ansible playbook, ensure the following prerequisites are met on the control node:

- Ansible is installed (Version 2.9 or higher)
- SSH access to the managed nodes is set up (password or key-based authentication)
- Managed nodes have internet access to pull Docker images from Docker Hub

## Getting Started

1. Clone this repository to your local machine:

```bash
https://github.com/adilansari488/ansible.git
```
and change directory to ansible/Minor-Project-1
```
cd ansible/Minor-Project-1
```

2. Modify the `hosts` file:

   In the `hosts` file, add the target hosts' IP addresses or hostnames where you want to deploy the httpd server.

3. Prepare your HTML code:

   Place your HTML code files that you want to serve in the httpd server inside the `html_code` directory.

4. Review and modify variables (optional):

   If you need to change the Docker image name, tag, or directories, you can do so by modifying the variables in the `vars.yml` file.

5. Run the Ansible playbook:

```bash
ansible-playbook main.yml
```

The playbook will connect to the managed nodes, configure Docker, pull the httpd server image from Docker Hub, copy your HTML code to the server, and start the httpd container exposed on port 80.

## Notes

- This playbook assumes that Docker is not installed on the managed nodes. If Docker is already installed, the playbook will not reinstall it.
- The playbook sets up the httpd container to listen on port 80. Make sure that port 80 is not occupied by other services on your managed nodes.

## Contributing

If you find any issues or have improvements to suggest, feel free to open a pull request. Contributions are always welcome!



