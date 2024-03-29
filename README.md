# Ansible role [etherpad](https://galaxy.ansible.com/ui/standalone/roles/buluma/etherpad/documentation)

Install and configure Etherpad on your system.

|GitHub|Version|Issues|Pull Requests|Downloads|
|------|-------|------|-------------|---------|
|[![github](https://github.com/buluma/ansible-role-etherpad/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-etherpad/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-etherpad.svg)](https://github.com/buluma/ansible-role-etherpad/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-etherpad.svg)](https://github.com/buluma/ansible-role-etherpad/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-etherpad.svg)](https://github.com/buluma/ansible-role-etherpad/pulls/)|[![Ansible Role](https://img.shields.io/ansible/role/d/buluma/etherpad)](https://galaxy.ansible.com/ui/standalone/roles/buluma/etherpad/documentation)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/buluma/ansible-role-etherpad/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  become: true
  gather_facts: true

  vars:
    etherpad_port: 9002

  roles:
    - role: buluma.etherpad
```

The machine needs to be prepared. In CI this is done using [`molecule/default/prepare.yml`](https://github.com/buluma/ansible-role-etherpad/blob/master/molecule/default/prepare.yml):

```yaml
---
- name: Prepare
  hosts: all
  gather_facts: false
  become: true

  roles:
    - role: buluma.bootstrap
    - role: buluma.core_dependencies
    - role: buluma.epel
    - role: buluma.npm
```

Also see a [full explanation and example](https://buluma.github.io/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/buluma/ansible-role-etherpad/blob/master/defaults/main.yml):

```yaml
---
# defaults file for etherpad

etherpad_version: "1.8.16"

etherpad_installation_destination: /opt

etherpad_port: 9001
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-etherpad/blob/master/requirements.txt).

## [State of used roles](#state-of-used-roles)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | Version |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Ansible Molecule](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-bootstrap.svg)](https://github.com/shadowwalker/ansible-role-bootstrap)|
|[buluma.core_dependencies](https://galaxy.ansible.com/buluma/core_dependencies)|[![Ansible Molecule](https://github.com/buluma/ansible-role-core_dependencies/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-core_dependencies/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-core_dependencies.svg)](https://github.com/shadowwalker/ansible-role-core_dependencies)|
|[buluma.epel](https://galaxy.ansible.com/buluma/epel)|[![Ansible Molecule](https://github.com/buluma/ansible-role-epel/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-epel/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-epel.svg)](https://github.com/shadowwalker/ansible-role-epel)|
|[buluma.npm](https://galaxy.ansible.com/buluma/npm)|[![Ansible Molecule](https://github.com/buluma/ansible-role-npm/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-npm/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-npm.svg)](https://github.com/shadowwalker/ansible-role-npm)|
|[buluma.service](https://galaxy.ansible.com/buluma/service)|[![Ansible Molecule](https://github.com/buluma/ansible-role-service/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-service/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-service.svg)](https://github.com/shadowwalker/ansible-role-service)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-etherpad/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|[Fedora](https://hub.docker.com/r/buluma/fedora)|all|
|[Ubuntu](https://hub.docker.com/r/buluma/ubuntu)|jammy|

The minimum version of Ansible required is 2.12, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-etherpad/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-etherpad/blob/master/CHANGELOG.md)

## [License](#license)

[Apache-2.0](https://github.com/buluma/ansible-role-etherpad/blob/master/LICENSE)

## [Author Information](#author-information)

[Shadow Walker](https://buluma.github.io/)
