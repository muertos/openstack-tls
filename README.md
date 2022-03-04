# Enable TLS in OpenStack using Ansible

WIP

# Setup

1. Authentication

Obtain `clouds.yaml` from your cloud. Ensure it's located as `/etc/openstack/clouds.yaml`.

2. Create a Python virtual environment

```
python3 -m venv .venv
source .venv/bin/activate
```

3. Install Python requirements

    pip install -r requirements.txt

4. Install Ansible Galaxy Collection

    ansible-galaxy collection install -r requirements.yml

# Configuration

Populate `./vars/globals.yml` with the needed configuration.

# Using

    ansible-playbook deploy.yml
