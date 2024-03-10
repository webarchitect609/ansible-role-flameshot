Ansible Role: Flameshot
=======================

[![Build Status](https://github.com/webarchitect609/ansible-role-flameshot/actions/workflows/build.yml/badge.svg)](https://github.com/webarchitect609/ansible-role-flameshot/actions/workflows/build.yml)
[![Latest version](https://img.shields.io/github/v/tag/webarchitect609/ansible-role-flameshot?sort=semver)](https://github.com/webarchitect609/ansible-role-flameshot/releases)

[![Downloads](https://img.shields.io/ansible/role/d/webarchitect609/flameshot)](https://galaxy.ansible.com/ui/standalone/roles/webarchitect609/flameshot)
[![License](https://img.shields.io/github/license/webarchitect609/ansible-role-flameshot)](LICENSE.md)
[![More stuff from me](https://img.shields.io/badge/galaxy-webarchitect609-000)](https://galaxy.ansible.com/ui/standalone/namespaces/7493/)

Compiles [Flameshot](https://flameshot.org/) ≥ `0.8.0`
from [the source code](https://github.com/lupoDharkael/flameshot) and installs it. Or just installs apt package.

Requirements
------------

[Flameshot dependencies for runtime and compilation](https://github.com/lupoDharkael/flameshot#dependencies) can be
found in the README file of the corresponding source repo.

Role Variables
--------------

See [defaults/main.yml](defaults/main.yml)

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: webarchitect609.flameshot }

License & Author Information
----------------------------

[BSD-3-Clause](LICENSE.md)
