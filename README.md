[![role](https://img.shields.io/ansible/role/54857)](https://galaxy.ansible.com/trallnag/keychain)
[![quality](https://img.shields.io/ansible/quality/54857)](https://galaxy.ansible.com/trallnag/keychain)
[![downloads](https://img.shields.io/ansible/role/d/54857?label=downloads)](https://galaxy.ansible.com/trallnag/keychain)

# Keychain

Install and configure Keychain ssh-agent mgmt utility.

Available on [Ansible Galaxy](https://galaxy.ansible.com/trallnag/keychain).

## Role Variables

```yaml
options:
  keychain_login_file:
    type: string
    required: false
    default: ~/.profile
    description: >-
      Path to the profile config script where the keychain init script is
      located. Usually "~/.profile" or "~/.bash_profile".
    
  keychain_args:
    type: string
    required: false
    default: --quick --quiet --timeout 60
    description: >-
      Arguments for keychain executable.
  keychain_used_shell:
    type: string
    required: false
    default: sh
    choices: ["sh", "fish", "csh"]
    description: >-
      Depending on this different files are sourced in the profile config
      script init block. 
```

## Example Playbook

```yaml
- name: Playbook
  hosts: myhost
  remote_user: myuser
  vars:
    rolespec_validate: true
  roles:
    - name: trallnag.keychain
      vars:
        keychain_login_file: ~/.bash_profile
        keychain_args: "--quick --quiet --timeout 60"
        keychain_used_shell: sh
```

## Special Requirements

None.

## Special Dependencies

None.

## License

Apache-2.0

## Author Information

Trallnag
