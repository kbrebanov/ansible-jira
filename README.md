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
| jira_version            | 6.4.5                                                            | Version of JIRA to install  |
| jira_archive_sha256sum  | b70ff0364e4c9be18b111e476c08aa22f705a1d48890318255874773be3b534a | SHA 256 checksum of archive |
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
