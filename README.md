Dependent software role
=========

An Ansible Role that installs packages, specified by `application_dependent_packages` list.

Example Playbook
----------------

    - hosts: all
      roles:
        - role: dependent-software
          application_dependent_packages:
            - curl
            - build-essential
            - git

License
-------

MIT

