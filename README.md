# ansible-role-setup

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-setup.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-setup)

RHEL/CentOS - Configure aliases, hostname, motd, and timezone

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    setup_aliases:
      root: /dev/null
    setup_proc_hidepid: '0'
    setup_timezone: PST8PDT

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.setup
          setup_aliases:
            root: taylor@linuxhq.org

## License

BSD

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
