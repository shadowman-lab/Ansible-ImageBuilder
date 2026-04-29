<!-- This was created with Claude Code -->

image_builder_apache_ssl
========================

An Ansible role for image builder apache ssl.

Requirements
------------

- Ansible 2.9 or higher
- Access to target systems with appropriate permissions

Role Variables
--------------

* **sslsetup**: Variable used in: Block for Apache SSL Setup
  - Default: `True`

* **certsourcelocation**: Variable used in: Copy Cert
  - Default: `/certs/shadowman_cert.cer`

* **keysourcelocation**: Variable used in: Copy Key
  - Default: `/certs/shadowman_private.key`

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: image_builder_apache_ssl
      vars:
        sslsetup: <value>
        certsourcelocation: <value>
        keysourcelocation: <value>
```

License
-------

GNU General Public License v3.0 or later

Author Information
------------------

Red Hat Ansible Automation Platform
