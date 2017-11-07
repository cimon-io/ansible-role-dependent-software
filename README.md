# Ansible dependent software role

An ansible role that updates the repository cache and installs packages, specified by the `software_packages_list` list.

This role can be run under all versions of Ubuntu.

## Requirements

None

## Role Variables

All necessary packages should be listed in software_packages_list:

```yaml
software_packages_list: []    # A list of packages to install
```

## Dependencies

None

## Example Playbook

A playbook example is given below:

```yaml
- hosts: all
  roles:
    - role: dependent-software
      software_packages_list:
        - "{{ base_packages }}"
        - postgresql-common
  vars:
    base_packages:
      - build-essential
      - wget
      - curl
      - git
      - rsync
      - jq
      - tmux
```

## License

Licensed under the [MIT License](https://opensource.org/licenses/MIT).
