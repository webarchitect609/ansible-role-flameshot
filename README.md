Ansible Role: Flameshot
=======================

[![Build Status](https://travis-ci.org/webarchitect609/ansible-role-flameshot.svg?branch=master)](https://travis-ci.org/webarchitect609/ansible-role-flameshot)

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

License
-------

MIT

Author Information
------------------

This role was created in 2020 by Gripinskiy Sergey.
