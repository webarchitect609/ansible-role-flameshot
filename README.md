WARNING! This role is deprecated and it's repo is archived!
-----------------------------------------------------------

### Reasons

1. The latest version of Flameshot can be easily [installed via Snap](https://snapcraft.io/flameshot). So there's no
   reason to compile it from the source anymore.
2. Moreover, it cannot be compiled in Ubuntu 18.04 LTS since `CMake >=3.13` is not available, only `3.10`.
3. Ubuntu `apt` installation method remains to be a bad option: it doesn't allow to install the latest version(for
   example `0.5.1` instead of `0.9.0` at the moment).

However, you can still use this role, compile or install old versions as much as you need to.

Ansible Role: Flameshot
===============================
[![Build Status](https://github.com/webarchitect609/ansible-role-flameshot/workflows/build/badge.svg?branch=master)](https://github.com/webarchitect609/ansible-role-flameshot/actions?query=workflow%3Abuild)
[![Latest version](https://img.shields.io/github/v/tag/webarchitect609/ansible-role-flameshot?sort=semver)](https://github.com/webarchitect609/ansible-role-flameshot/releases)
[![Downloads](https://img.shields.io/ansible/role/d/39614)](https://galaxy.ansible.com/webarchitect609/flameshot)
[![License](https://img.shields.io/github/license/webarchitect609/ansible-role-flameshot)](LICENSE.md)
[![More stuff from me](https://img.shields.io/badge/galaxy-webarchitect609-000)](https://galaxy.ansible.com/webarchitect609)

Installs [Flameshot](https://flameshot.js.org) or compiles it
from [the source code](https://github.com/lupoDharkael/flameshot), but only <= `0.6.0`.

Requirements
------------

[Flameshot dependencies for runtime or compilation](https://github.com/lupoDharkael/flameshot#dependencies) can be found
in the README file of the source repo.

Role Variables
--------------

None of the variables need to be altered for installing the latest stable version of the application. However, all
available variables are listed below, along with default values (see `defaults/main.yml`):

    flameshot_compile: false

If true Flameshot will be compiled from the sources.

    flameshot_compile_version: v0.6.0

Which version(git tag) or branch to compile. Active only when `flameshot_compile: true`. Note, that Flameshot is
switched from `qmake` to `cmake` after `0.6.0`. **This role doesn't support `cmake` compiling**.

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
