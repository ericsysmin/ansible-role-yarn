# ericsysmin.yarn

[![Build Status](https://travis-ci.com/ericsysmin/ansible-role-yarn.png?branch=master)](https://travis-ci.com/ericsysmin/ansible-role-yarn)

Ansible package to install yarn package manager on a host

## Requirements

```yaml
- role: ericsysmin.epel
- role: geerlingguy.nodejs
```

## Role Variables

| Variable                   | Required | Default                                                  | Comments              |
| -------------------------- | -------- | -------------------------------------------------------- | --------------------- |
| `yarn_release`             | Optional | `stable`                                                 | yarn version          |
| `yarn_debian_repo_url`     | Optional | `https://dl.yarnpkg.com/debian/ {{ yarn_release }} main` | Debian repository url |
| `yarn_debian_repo_gpg_key` | Optional | `https://dl.yarnpkg.com/debian/pubkey.gpg`               | Debian repository key |
| `yarn_rhel_repo_url`       | Optional | `https://dl.yarnpkg.com/rpm/`                            | Redhat repostiroy url |
| `yarn_rhel_repo_gpg_key`   | Optional | `https://dl.yarnpkg.com/rpm/pubkey.gpg`                  | Redhat repostiroy key |

## Example Playbook

Including an example of how to use your role (for instance, with variables
passed in as parameters) is always nice for users too:

```yaml
- hosts: servers
  roles:
     - role: ericsysmin.yarn
```

## License

BSD

## Author Information

[ericsysmin](https://ericsysmin.com)
