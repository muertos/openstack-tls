# Enable TLS in OpenStack using Ansible

WIP

# Setup

#. Authentication

Obtain `clouds.yaml` from your cloud. Ensure it's located as `/etc/openstack/clouds.yaml`.

#. Create a Python virtual environment

    python3 -m venv .venv
    source .venv/bin/activate

#. Install Python requirements

    pip install -r requirements.txt

#. Install Ansible Galaxy Collection

    ansible-galaxy collection install -r requirements.yml

# Configuration

Populate `./vars/globals.yml` with the needed configuration.

# Using

    ansible-playbook deploy.yml
