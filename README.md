# Ansible Role: ansible-apps_glusterfs_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_glusterfs_exporter.svg?branch=master?style=flat)](https://travis-ci.com/lotusnoir/ansible-apps_glusterfs_exporter)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)
[![Ansible Role](https://img.shields.io/badge/galaxy-apps_glusterfs_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_glusterfs_exporter)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_glusterfs_exporter?color=orange&style=flat)
![Ansible Quality Score](https://img.shields.io/ansible/quality/52300)
[![downloads](https://img.shields.io/ansible/role/d/52300)](https://galaxy.ansible.com/lotusnoir/apps_glusterfs_exporter)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_glusterfs_exporter.svg)](https://github.com/lotusnoir/ansible-apps_glusterfs_exporter/releases/)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_glusterfs_exporter&metric=alert_status)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_glusterfs_exporter)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_glusterfs_exporter&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_glusterfs_exporter)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_glusterfs_exporter&metric=reliability_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_glusterfs_exporter)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_glusterfs_exporter&metric=security_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_glusterfs_exporter)

Deploy [glusterfs_exporter](https://github.com/gluster/gluster-prometheus) to expose glusterfs metrics to prometheus.

## Role variables

| Name                               | Default Value             | Description                        |
| ---------------------------------- | ------------------------- | -----------------------------------|
| `gluster_exporter_version`         | 0.1.0                     | exporter version |
| `glusterfs_exporter_install_dir`   | /usr/local/bin            | exporter binary install dir |
| `glusterfs_exporter_force_install` | false                     | force exporter install |
| `glusterfs_exporter_listen_port`   | 9129                      | port to expose prometheus metrics |
| `gluster_exporter_metrics_path`    | /metrics                  | metrics expose path |
| `gluster_exporter_gluster_binary`  | /usr/sbin/gluster         | gluster binary |
| `gluster_exporter_log_dir`         | /var/log/gluster-exporter | log directory |
| `gluster_exporter_log_file`        | exporter.log              | exporter log filename |
| `gluster_exporter_log_level`       | info                      | exporter log level |

## Examples

	---
	- hosts: apps_glusterfs_exporter
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_glusterfs_exporter
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.
