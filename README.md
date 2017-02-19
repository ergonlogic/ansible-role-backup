# Ansible Role: Backup

[![Build Status](https://travis-ci.org/ergonlogic/ansible-role-backup.svg?branch=master)](https://travis-ci.org/ergonlogic/ansible-role-backup)

A flexible backup system based on [Restic](https://restic.github.io/), and
[BackupNinja](https://0xacab.org/riseuplabs/backupninja). It currently uses
[Amazon S3](https://aws.amazon.com/s3/) for off-site storage, though Restic's
[SFTP](https://restic.readthedocs.io/en/stable/Manual/#create-an-sftp-repository),
[Rest Server](https://github.com/restic/rest-server) and
[Minio](https://www.minio.io/) support are planned.

## Requirements

At present, this role assumes that it will be provisioning one or more S3 buckets as offsite storage backends. As a result, Amazon Web Services (AWS) credentials are required. See [Ansible's AWS Guide](http://docs.ansible.com/ansible/guide_aws.html#authentication) guide for instructions on authenticating to AWS.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):


## Dependencies


## Example Playbook

    - hosts: all
      roles:
        - ergonlogic.backup

## License

MIT / BSD

## Author Information

This role was created in 2017 by [Christopher Gervais](http://ergonlogic.com/), lead maintainer of the [Aegir Hosting System](http://www.aegirproject.org).
