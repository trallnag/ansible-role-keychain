# Keychain

Keychain for managing ssh-agent. Installs APT package and adds block to login
script file. Allows modification via variables. Can be set to `present` and
`absent` and therefore supports deinstallation.

Available on [Ansible Galaxy](https://galaxy.ansible.com/trallnag/keychain).

## Requirements

None.

## Role Variables

| Name            | Default                        | Description                                                                      |
| --------------- | ------------------------------ | -------------------------------------------------------------------------------- |
| `state`         | `present`                      | If keychain should be present or not. Allowed values are `present` and `absent`. |
| `login_file`    | `~/.profile`                   | In what file should the init block for keychain be placed?                       |
| `keychain_args` | `"--quick --quiet --timeout 60"` | Args passed to keychain                                                          |

## Dependencies

None.

## Example Playbook

```yaml
- name: "Example"
  hosts: myhost
  remote_user: myuser
  roles:
    - name: trallnag.keychain
      vars:
        state: present
        login_file: ~/.bash_profile
        keychain_args: "--quick --quiet --timeout 60"
```

## License

MIT
