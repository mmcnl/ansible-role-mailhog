## Usage

To check captured messages, run this command on your local machine to create a
SSH tunnel into server, then visit http://localhost:8025/. if this server is
outside your local network, you may have to open the firewall and forward a port
```
ssh -f -N -L 8025:localhost:8025 example.com
```

## Example Playbook

    - hosts: all
      tasks:
        - import_role:
            name: mmcnl.mailhog
          vars:
            # if not enabled, mailhog will still be installed but just not started automatically by systemd
            mailhog_enabled: yes 

## License

MIT

