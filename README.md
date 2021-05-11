ansible-graylog-alert-exporter
=========

Install graylog alert exporter using ansible.

Requirements
------------

- Ansible >= 2.10

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Example Playbook
----------------

```yaml
- hosts: all
  gather_facts: true
  roles:
    - ansible-graylog-alert-exporter
```

## Local Testing
These steps are use to locally testing the role with [molecule](https://github.com/ansible-community/molecule).

1. Install test requirements via `pip install -r test-requirements.txt`.

2. Simple run `molecule test`.

> You can test all step with wrapper use  
> `$ tox`   
> and configure in **tox.ini**

License
-------

MIT

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
