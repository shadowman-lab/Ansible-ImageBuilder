<!-- This was created with Claude Code -->

image_builder_setup_sat
=======================

An Ansible role for image builder setup sat.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **rhsatellite**: Variable used in: Block for Sat Setup
  - Default: `True`

* **sat_host**: Target host or hostname
  - Default: `sat6.shadowman.dev`

* **sat_organization**: Organization name or identifier
  - Default: `Shadowman`

* **sat_environment**: Environment name or configuration
  - Default: `Production`

* **sat_contentview**: Content data
  - Default: `RHEL8`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: image_builder_setup_sat
      vars:
        rhsatellite: <value>
        sat_host: <value>
        sat_organization: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
