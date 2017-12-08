# ansible-role-setup

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-setup.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-setup)

RHEL/CentOS - Configure aliases, hostname, securetty, shells and more

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    setup_aliases: []
    setup_environment: []
    setup_hosts: []
    setup_hostname: "{{ inventory_hostname }}"
    setup_motd: ''
    setup_profile_d: []
    setup_securetty:
      - console
      - hvc0
      - tty1
      - xvc0
    setup_shells:
      - /bin/sh
      - /bin/bash
      - /sbin/nologin
      - /usr/bin/sh
      - /usr/bin/bash
      - /usr/sbin/nologin

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.setup
          setup_aliases:
            - name: root
              value:
                - /dev/null

## License

GPLv3

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
