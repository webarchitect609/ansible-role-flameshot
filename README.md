Ansible Role: Flameshot
===============================
[![Build Status](https://github.com/webarchitect609/ansible-role-flameshot/workflows/build/badge.svg?branch=master)](https://github.com/webarchitect609/ansible-role-flameshot/actions?query=workflow%3Abuild)
[![Latest version](https://img.shields.io/github/v/tag/webarchitect609/ansible-role-flameshot?sort=semver)](https://github.com/webarchitect609/ansible-role-flameshot/releases)
[![Downloads](https://img.shields.io/ansible/role/d/39614)](https://galaxy.ansible.com/webarchitect609/flameshot)
[![License](https://img.shields.io/github/license/webarchitect609/ansible-role-flameshot)](LICENSE.md)
[![More stuff from me](https://img.shields.io/badge/galaxy-webarchitect609-000)](https://galaxy.ansible.com/webarchitect609)

Installs [Flameshot](https://flameshot.js.org) or compiles it from [the source code](https://github.com/lupoDharkael/flameshot).    

Requirements
------------

[Flameshot dependencies for runtime or compilation](https://github.com/lupoDharkael/flameshot#dependencies) can be
found in the README file of the source repo. 

Role Variables
--------------

None of the variables need to be altered for installing the latest stable version of the application.
However, all available variables are listed below, along with default values (see `defaults/main.yml`):

    flameshot_compile: false

If true Flameshot will be compiled from the sources.

    flameshot_compile_version: master

Which version(git tag) or branch to compile. Active only when `flameshot_compile: true`.

    flameshot_source_repo: "https://github.com/lupoDharkael/flameshot.git"

Which git repo use to compile from. Active only when `flameshot_compile: true`.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: webarchitect609.flameshot }

License & Author Information
-------
[BSD-3-Clause](LICENSE.md)
