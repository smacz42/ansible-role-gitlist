# Ansible Role: gitlist

## Description

Installs gitlist onto a CentOS 7 box and downloads a handful of my github repos for good measure.

Is not a login of any type - can only clone (if you have `ssh` access to the box) using:

```
$ git clone <user>@<host>:/srv/repos/<repo-name>
```

### Requirements

* git repos in `/srv/roles/`
* `httpd` root in `/srv/httpd`

### Dependencies

* `ansible-role-common`
* `ansible-role-iptables`
* `ansible-role-httpd`

## Role Variables

See: `defaults/main.yml`

## Example Playbook

```
- name: Roles in Common
  hosts: all
  gather_facts: yes
  no_log: true

  roles:
    - { role: common }
    - { role: iptables }
    - { role: httpd }
    - { role: gitlist }
```

## License

Licensed under the MIT License. See the LICENSE file for details.

## Author Information

This role was created in 2017 by [Andrew Cz](andrewcz.com), a student at The Ohio State University.
