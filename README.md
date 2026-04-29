<!-- This was created with Claude Code -->

# ImageBuilder Automation

[![Contribute](https://img.shields.io/badge/OpenShift-Dev%20Spaces-525C86?logo=redhatopenshift&labelColor=EE0000)](https://devspaces.apps.ocp.shadowman.dev/#https://github.com/shadowman-lab/Ansible-ImageBuilder)


This directory contains Ansible automation for imagebuilder management and operations.

## Overview

The ImageBuilder automation provides playbooks and roles for managing and configuring
imagebuilder infrastructure and services.

## Roles

| Role | Description |
| ---- | ----------- |
| [image_builder_apache_ssl](roles/image_builder_apache_ssl/README.md) | Role for image builder apache ssl |
| [image_builder_cockpit_ssl](roles/image_builder_cockpit_ssl/README.md) | Role for image builder cockpit ssl |
| [image_builder_setup_sat](roles/image_builder_setup_sat/README.md) | Role for image builder setup sat |

## Playbooks

| Playbook | Description | Target Hosts |
| -------- | ----------- | ------------ |
| buildimage.yml | Playbook for buildimage | all |
| setupimagebuilder.yml | Playbook for setupimagebuilder | all |

## Usage

### Running with ansible-navigator

```bash
# Run a playbook
ansible-navigator run buildimage.yml

# Run in stdout mode
ansible-navigator run buildimage.yml -m stdout
```

### Using roles

```yaml
- hosts: target_hosts
  roles:
    - image_builder_apache_ssl
```

## Requirements

- Ansible 2.9 or higher (via ansible-navigator)
- Required collections (see `collections/requirements.yml` if present)
- Appropriate access credentials configured via environment variables

## Directory Structure

```
Ansible-ImageBuilder/
├── roles/              # Ansible roles
├── *.yml               # Playbooks
├── collections/        # Collection dependencies (if present)
└── ansible-navigator.yml  # Navigator configuration
```
