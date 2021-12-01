# ansible-apps_glusterfs_exporter

## Description

[![Galaxy Role](https://img.shields.io/badge/galaxy-apps_glusterfs_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_glusterfs_exporter)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_glusterfs_exporter.svg)](https://github.com/lotusnoir/ansible-apps_glusterfs_exporter/releases/latest)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_glusterfs_exporter?color=orange&style=flat)
[![downloads](https://img.shields.io/ansible/role/d/56083)](https://galaxy.ansible.com/lotusnoir/apps_glusterfs_exporter)
![Ansible Quality Score](https://img.shields.io/ansible/quality/56083)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)

Deploy [glusterfs_exporter](https://github.com/gluster/gluster-prometheus) to expose glusterfs metrics to prometheus.

## Requirements

none

## Role variables

See [variables](/defaults/main.yml) for more details.

## Examples

        ---
        - hosts: apps_glusterfs_exporter
          become: true
          become_method: sudo
          gather_facts: true
          roles:
            - role: ansible-apps_glusterfs_exporter


## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.

