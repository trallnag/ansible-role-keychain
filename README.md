# Keychain

Keychain for managing ssh-agent. Installs APT package and adds block to login
script file. Allows modification via variables. Can be set to `present` and
`absent` and therefore supports deinstallation.

Available on [Ansible Galaxy](https://galaxy.ansible.com/trallnag/keychain).

## Requirements

* Ubuntu only. Only tested on "vanilla" Ubuntu server starting with 20.04.
* System should be more or less vanilla. Systemd must be used. 

## Role Variables

| Name            | Allowed             | Default                          | Description                                                 |
| --------------- | ------------------- | -------------------------------- | ----------------------------------------------------------- |
| `state`         | `present`, `absent` | `present`                        | If keychain should be present or not.                       |
| `login_file`    | Path to file        | `~/.profile`                     | In what file should the init block for keychain be placed?  |
| `keychain_args` | String              | `"--quick --quiet --timeout 60"` | Args passed to keychain                                     |
| `used_shell`    | `sh`, `csh`, `fish` | `sh`                             | Set the file that should be sourced containing socket info. |

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
        used_shell: sh
```

## License

MIT
