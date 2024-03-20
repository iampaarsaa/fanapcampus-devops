# Ansible Project: Server Hardening and Docker Registry Setup

This Ansible project automates the process of server hardening followed by setting up a private local Docker registry. The registry acts as a cache registry and facilitates obtaining Docker images for services like Nginx, MySQL, and WordPress.

## Requirements
- Ansible installed on the controller node(s)

## Execution Steps
1. **Server Hardening:**
    - Execute server hardening tasks to enhance server security.

2. **Setting up Private Local Docker Registry:**
    - Docker up a private local registry which serves as a cache registry.
    - Obtain necessary Docker images from Docker Hub and the cache private registry.

3. **Obtaining Docker Images:**
    - Pull Nginx image from Docker Hub.
    - Obtain Docker images of MySQL and WordPress from the cache private registry.

4. **Private Cached Registries:**
    - Registry URL: registry.mahmoudisari.ir
    - WordPress URL: wordpress.mahmoudisari.ir

## Usage
1. Ensure Ansible is installed on your controller node(s).
2. Clone this repository to your local machine.
3. Put the Vault's password in [.secrets](.secrets) file
4. Modify the Ansible playbook and inventory files according to your server configurations.
5. Run the Ansible playbook:
    ```bash
    ANSIBLE_CONFIG=./ansible.cfg ansible-playbook -i inventory/hosts.yaml playbook.yaml
    ```

## Note
- Make sure to adjust playbook and inventory files as per your environment setup.
- Ensure proper network configurations to access the private cached registries.
