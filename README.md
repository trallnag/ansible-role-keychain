[![role](https://img.shields.io/ansible/role/54857)](https://galaxy.ansible.com/trallnag/keychain)
[![quality](https://img.shields.io/ansible/quality/54857)](https://galaxy.ansible.com/trallnag/keychain)
[![downloads](https://img.shields.io/ansible/role/d/54857?label=downloads)](https://galaxy.ansible.com/trallnag/keychain)

# Keychain

Install and configure Keychain ssh-agent mgmt utility.

Available on [Ansible Galaxy](https://galaxy.ansible.com/trallnag/keychain).

## Role Variables

```yaml
# Path to the profile config script where the keychain init script is located.
# Usually "~/.profile" or "~/.bash_profile".
login_file: ~/.profile

# Arguments for keychain executable.
keychain_args: "--quick --quiet --timeout 60"

# Depending on this different files are sourced in the profile config scrip
# init block.
# Choose from "sh", "fish", "csh".
used_shell: sh
```

## Example Playbook

```yaml
- name: Playbook
  hosts: myhost
  remote_user: myuser
  roles:
    - name: trallnag.keychain
      vars:
        login_file: ~/.bash_profile
        keychain_args: "--quick --quiet --timeout 60"
        used_shell: sh
```

## Special Requirements

None.

## Special Dependencies

None.

## License

Apache-2.0

## Author Information

Trallnag
