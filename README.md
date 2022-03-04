# Enable TLS in OpenStack using Ansible

WIP

This currently handles:

- Creates a private network and subnet
- Creates an instance on that private network and subnet

TODO:

- Install NGINX to the instance
- Configure NGINX with a specified domain

The idea is that when the above steps are complete, you are now poised to use
Kolla Ansible to reconfigure your cloud with TLS on the public domain name.

## Setup

1. Authentication

   Obtain `clouds.yaml` from your cloud. Ensure it's located as `/etc/openstack/clouds.yaml`. Your password must be hardcoded into this file.

TODO: prefer token auth over using password

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
