# home-ansible

Automation and configuration management for my home infrastructure using
**Ansible**.

This repository contains playbooks, roles, and inventory definitions
used to configure and maintain systems in my home lab. It is designed to
automate system setup, enforce configuration standards, and simplify
repeatable infrastructure tasks.

Typical use cases include:

-   Initial system provisioning
-   Configuration management
-   Package installation
-   Service configuration
-   Home lab infrastructure automation

------------------------------------------------------------------------

# Architecture

This repository follows a typical Ansible project structure:

home-ansible/ ├── inventory/ │ ├── hosts.yml │ └── group_vars/ ├──
host_vars/ ├── playbooks/ │ ├── site.yml │ ├── workstation.yml │ ├──
server.yml │ └── network.yml ├── roles/ │ ├── common/ │ ├── docker/ │
├── monitoring/ │ └── security/ ├── files/ ├── templates/ ├──
ansible.cfg └── requirements.yml

## Key Components

### Inventory

Defines managed hosts and groups.

Example:

``` yaml
all:
  children:
    servers:
      hosts:
        nas01:
        proxmox01:
    workstations:
      hosts:
        macbook:
        workstation01:
```

------------------------------------------------------------------------

### Playbooks

Playbooks define orchestration tasks across hosts.

Example run:

``` bash
ansible-playbook -i inventory/hosts.yml playbooks/site.yml
```

------------------------------------------------------------------------

### Roles

Roles organize reusable automation logic.

Example roles may include:

roles/common\
roles/docker\
roles/security\
roles/monitoring

Roles allow modular automation for:

-   OS configuration
-   Package installation
-   Container setup
-   User management
-   Security hardening

------------------------------------------------------------------------

# Requirements

Controller machine:

-   Python 3.9+
-   Ansible 2.14+
-   SSH access to target machines
-   SSH key authentication recommended

Install Ansible:

``` bash
pip install ansible
```

or

``` bash
brew install ansible
```

------------------------------------------------------------------------

# Setup

## 1. Clone the repository

``` bash
git clone https://github.com/StrangeDaize/home-ansible.git
cd home-ansible
```

## 2. Install required roles

If using Galaxy roles:

``` bash
ansible-galaxy install -r requirements.yml
```

------------------------------------------------------------------------

## 3. Configure SSH access

Ensure passwordless SSH is working:

``` bash
ssh-copy-id user@host
```

Test connectivity:

``` bash
ansible all -i inventory/hosts.yml -m ping
```

------------------------------------------------------------------------

# Running Playbooks

Run the main site playbook:

``` bash
ansible-playbook -i inventory/hosts.yml playbooks/site.yml
```

Run against a specific host:

``` bash
ansible-playbook -i inventory/hosts.yml playbooks/site.yml --limit nas01
```

Run with privilege escalation:

``` bash
ansible-playbook -i inventory/hosts.yml playbooks/site.yml -K
```

------------------------------------------------------------------------

# Secrets Management

Sensitive values should be stored using **Ansible Vault**.

Encrypt a file:

``` bash
ansible-vault encrypt group_vars/all/vault.yml
```

Run playbook with vault:

``` bash
ansible-playbook playbooks/site.yml --ask-vault-pass
```

------------------------------------------------------------------------

# Example Use Cases

This repository can automate tasks such as:

-   Initial Linux server setup
-   Installing Docker and container services
-   Deploying monitoring tools
-   Configuring SSH and security policies
-   Maintaining consistent system configuration

------------------------------------------------------------------------

# Future Improvements

-   CI pipeline for playbook linting
-   Automated testing with Molecule
-   Infrastructure diagrams
-   Dynamic inventory integration
-   GitOps workflow for home infrastructure

------------------------------------------------------------------------

# License

MIT License
