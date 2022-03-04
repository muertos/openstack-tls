# Enable TLS in OpenStack using Ansible with Certbot

WIP

The idea is to aid in enabling TLS in an OpenStack cloud using a certbot
instance.

This playbook currently handles:

- Creates a private network and subnet
- Creates an instance on that private network and subnet

TODO:

- Install NGINX to the instance
- Configure NGINX with a specified domain

## Setup

1. Authentication (TODO: prefer token auth over using password)

   Obtain `clouds.yaml` from your cloud. Ensure it's located as `/etc/openstack/clouds.yaml`. Your password must be hardcoded into this file.

2. Create a Python virtual environment

   ```
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. Install Python requirements

   ```
   pip install -r requirements.txt
   ```

4. Install Ansible Galaxy Collection

   ```
   ansible-galaxy collection install -r requirements.yml
   ```

## Configuration

Populate `./vars/globals.yml` with the needed configuration.

## Using

```
ansible-playbook deploy.yml
```
