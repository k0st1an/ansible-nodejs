# Ansible NodeJS

[![Build Status](https://travis-ci.org/k0st1an/ansible-nodejs.svg?branch=master)](https://travis-ci.org/k0st1an/ansible-nodejs) [![Ansible Galaxy](https://img.shields.io/badge/galaxy-k0st1an.nodejs-blue.svg?style=flat)](https://galaxy.ansible.com/k0st1an/nodejs/)

This role set up latest version NodeJS (7.x).

## Role Variables

Available variable:

```yaml
nodejs_build_essential: true
```

## Example Playbook

You can create a few files for using this role. `pb.yml`:

```yaml
---
- hosts: test
  become: yes
  roles:
    - ansible-nodejs
```

`ansible.cfg`:

```
[defaults]
roles_path=../
ask_sudo_pass = True
inventory = hosts
```

`hosts`:

```
[test]
a.b.c.d
```

And run this playbook:

```
$ ansible-playbook pb.yml
...
```

## License

MIT

## Author Information

- Author: Konstantin Kruglov
- GitHub: https://github.com/k0st1an
- Contact: kruglovk@gmail.com
