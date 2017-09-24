ENiGMA½ BBS [![Build Status](https://travis-ci.org/davestephens/ansible-role-engima-bbs.svg?branch=master)](https://travis-ci.org/davestephens/ansible-role-engima-bbs) 
===========
Installs [ENiGMA½ BBS software](https://github.com/NuSkooler/enigma-bbs). 

Requirements
------------

Ubuntu or Debian based Linux distribution. A Raspberry Pi with Raspbian installed is a great candidate!

Role Variables
--------------

````yaml
enigma_home: "{{ ansible_env.HOME }}/enigma_bbs" # ENiGMA½ install path
enigma_repo: https://github.com/NuSkooler/enigma-bbs # ENiGMA½ repo to use

nvm_version: v0.33.4 # nvm version to use
nvm_node_version: 6.11.3 # node version to install (must be a full version number and not an alias)
````
Dependencies
------------

    - leonidas.nvm - nvm installation.

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: davestephens.enigma-bbs }

Testing
-------
The role is tested against Debian and Ubuntu with [Travis CI](https://travis-ci.org/davestephens/ansible-role-engima-bbs).

License
-------

MIT

Author Information
------------------
[David Stephens](http://www.davidstephens.uk) - a DevOps and platform engineer from London, UK.
