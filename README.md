# [Ansible role vault_oracle_plugin](#vault_oracle_plugin)

Installs the vault_plugin-database-oracle on your system.

|GitHub|GitLab|Downloads|Version|
|------|------|---------|-------|
|[![github](https://github.com/robertdebock/ansible-role-vault_oracle_plugin/workflows/Ansible%20Molecule/badge.svg)](https://github.com/robertdebock/ansible-role-vault_oracle_plugin/actions)|[![gitlab](https://gitlab.com/robertdebock-iac/ansible-role-vault_oracle_plugin/badges/master/pipeline.svg)](https://gitlab.com/robertdebock-iac/ansible-role-vault_oracle_plugin)|[![downloads](https://img.shields.io/ansible/role/d/robertdebock/vault_oracle_plugin)](https://galaxy.ansible.com/robertdebock/vault_oracle_plugin)|[![Version](https://img.shields.io/github/release/robertdebock/ansible-role-vault_oracle_plugin.svg)](https://github.com/robertdebock/ansible-role-vault_oracle_plugin/releases/)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/robertdebock/ansible-role-vault_oracle_plugin/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  become: true
  gather_facts: true

  roles:
    - role: robertdebock.vault_oracle_plugin
```

The machine needs to be prepared. In CI this is done using [`molecule/default/prepare.yml`](https://github.com/robertdebock/ansible-role-vault_oracle_plugin/blob/master/molecule/default/prepare.yml):

```yaml
---
- name: Prepare
  hosts: all
  become: true
  gather_facts: false

  roles:
    - role: robertdebock.bootstrap
    - role: robertdebock.core_dependencies
    - role: robertdebock.oracle_instant_client
      oracle_instant_client_version: "19.17.0.0.0"
```

Also see a [full explanation and example](https://robertdebock.nl/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/robertdebock/ansible-role-vault_oracle_plugin/blob/master/defaults/main.yml):

```yaml
---
# defaults file for vault_oracle_plugin

# The path where to install this plugin.
vault_plugin_oracle_directory: /opt/vault/plugins

# The version of the plugin to install. See https://releases.hashicorp.com/vault-plugin-database-oracle/ .
vault_plugin_oracle_version: 0.9.0
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/robertdebock/ansible-role-vault_oracle_plugin/blob/master/requirements.txt).

## [State of used roles](#state-of-used-roles)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | GitLab |
|-------------|--------|--------|
|[robertdebock.bootstrap](https://galaxy.ansible.com/robertdebock/bootstrap)|[![Build Status GitHub](https://github.com/robertdebock/ansible-role-bootstrap/workflows/Ansible%20Molecule/badge.svg)](https://github.com/robertdebock/ansible-role-bootstrap/actions)|[![Build Status GitLab](https://gitlab.com/robertdebock-iac/ansible-role-bootstrap/badges/master/pipeline.svg)](https://gitlab.com/robertdebock-iac/ansible-role-bootstrap)|
|[robertdebock.core_dependencies](https://galaxy.ansible.com/robertdebock/core_dependencies)|[![Build Status GitHub](https://github.com/robertdebock/ansible-role-core_dependencies/workflows/Ansible%20Molecule/badge.svg)](https://github.com/robertdebock/ansible-role-core_dependencies/actions)|[![Build Status GitLab](https://gitlab.com/robertdebock-iac/ansible-role-core_dependencies/badges/master/pipeline.svg)](https://gitlab.com/robertdebock-iac/ansible-role-core_dependencies)|
|[robertdebock.oracle_instant_client](https://galaxy.ansible.com/robertdebock/oracle_instant_client)|[![Build Status GitHub](https://github.com/robertdebock/ansible-role-oracle_instant_client/workflows/Ansible%20Molecule/badge.svg)](https://github.com/robertdebock/ansible-role-oracle_instant_client/actions)|[![Build Status GitLab](https://gitlab.com/robertdebock-iac/ansible-role-oracle_instant_client/badges/master/pipeline.svg)](https://gitlab.com/robertdebock-iac/ansible-role-oracle_instant_client)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://robertdebock.nl/) for further information.

Here is an overview of related roles:
![dependencies](https://raw.githubusercontent.com/robertdebock/ansible-role-vault_oracle_plugin/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/robertdebock):

|container|tags|
|---------|----|
|[Debian](https://hub.docker.com/r/robertdebock/debian)|all|
|[EL](https://hub.docker.com/r/robertdebock/enterpriselinux)|9|
|[Ubuntu](https://hub.docker.com/r/robertdebock/ubuntu)|jammy, focal|

The minimum version of Ansible required is 2.12, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/robertdebock/ansible-role-vault_oracle_plugin/issues).

## [License](#license)

[Apache-2.0](https://github.com/robertdebock/ansible-role-vault_oracle_plugin/blob/master/LICENSE).

## [Author Information](#author-information)

[robertdebock](https://robertdebock.nl/)

Please consider [sponsoring me](https://github.com/sponsors/robertdebock).
