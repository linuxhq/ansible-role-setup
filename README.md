# ansible-role-setup

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-setup.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-setup)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-setup-blue.svg?style=flat)](https://galaxy.ansible.com/linuxhq/setup)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

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

Copyright (C) 2018 Taylor Kimball <tkimball@linuxhq.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
