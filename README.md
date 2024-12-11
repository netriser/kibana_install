# Kibana Install Role

An Ansible role to install and configure Kibana on supported platforms.

## Features
- Installs Kibana on Debian- or RHEL-based systems.
- Configures Kibana for integration with Elasticsearch.
- Manages Kibana service for startup and runtime configuration.

## Requirements
- Ansible 2.9 or higher.
- Supported platforms:
  - **Debian-based systems:** Debian, Ubuntu.
  - **RHEL-based systems:** CentOS, Rocky Linux, etc.
- Elasticsearch must be installed and running for Kibana to connect to.

## Role Variables
The following variables can be customized for this role:

### Defaults
Located in `defaults/main.yml`:
```yaml
# Default Kibana version
kibana_version: "8.10.1"
```

Exemple playbook
```yaml
# Exemple playbook
- name: Install Kibana cluster
  hosts: all
  become: yes
  gather_facts: yes
  vars:
    kibana_version: "8.10.1"

  roles:
  - kibana_install
```

## Dependencies
None.

## License
MIT

## Author Information
This role was created by Chakib. Contributions and feedback are welcome!