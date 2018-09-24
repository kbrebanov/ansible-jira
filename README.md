[![No Maintenance Intended](http://unmaintained.tech/badge.svg)](http://unmaintained.tech/)

jira
====

[![Ansible Role](https://img.shields.io/ansible/role/3981.svg)](https://galaxy.ansible.com/list#/roles/3981)

Installs JIRA.

Requirements
------------

This role requires Ansible 1.6 or higher.

Role Variables
--------------

| Name                    | Default                                                          | Description                 |
|-------------------------|------------------------------------------------------------------|-----------------------------|
| jira_version            | 6.4.12                                                           | Version of JIRA to install  |
| jira_archive_sha256sum  | a77cf4c646d3f49d3823a5739daea0827adad1254dae1d1677c629e512a7afd4 | SHA 256 checksum of archive |
| jira_jvm_minimum_memory | 384m                                                             | JIRA JVM minimum memory     |
| jira_jvm_maximum_memory | 768m                                                             | JIRA JVM maximum memory     |

Dependencies
------------

- kbrebanov.java (Java 8)

Example Playbook
----------------

Install JIRA
```
- hosts: all
  roles:
    - { role: kbrebanov.jira }
```

Install JIRA specifying version
```
- hosts: all
  roles:
    - { role: kbrebanov.jira, jira_version: 6.4.4, jira_archive_sha256sum: 84e51eb3064c0d4f9797b5f3c1aa8ef9a5430d8b95dd07e0f4b8bb1ec06eb316 }
```

Install JIRA specifying JIRA JVM memory
```
- hosts: all
  roles:
    - { role: kbrebanov.jira, jira_jvm_minimum_memory: 3000m, jira_jvm_maximum_memory: 4096m }
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
