[![Build Status](https://img.shields.io/travis/ptavares/ansible-role-kubectl/master.svg?style=flat-square)](https://travis-ci.org/ptavares/ansible-role-kubectl)
[![Ansible Role](https://img.shields.io/ansible/role/42849.svg)](https://galaxy.ansible.com/ptavares/ansible-role-kubectl)
[![Ansible Role](https://img.shields.io/ansible/quality/42849.svg)](https://galaxy.ansible.com/ptavares/ansible-role-kubectl)
[![Ansible Role](https://img.shields.io/ansible/role/d/42849.svg)](https://galaxy.ansible.com/ptavares/ansible-role-kubectl)
[![License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](https://github.com/ptavares/ansible-role-kubectl/blob/master/LICENSE)

ansible-role-kubectl
=========

Ansible role for installating kubectl CLI

Requirements
------------

Only test with ansible 2.5 min version

Role Variables
--------------
Available variables are listed below, along with default values (see [defaults/main.yml](https://github.com/ptavares/ansible-role-kubectl/blob/master/defaults/main.yml)):

### Kubectl version 

```yaml
# By default, module will download last version
# To specify a version, use this below param
# kubectl_install_version: vX.X.X

# URL to retrieve last stable kubectl release version
kubectl_last_version_info_url: https://storage.googleapis.com/kubernetes-release/release/stable.txt
```
### Download information

```yaml
# Directory where executable will be downloaded before installation
kubectl_download_location: /tmp/
# Url to packer zip
kubectl_url: "https://storage.googleapis.com/kubernetes-release/release/{{ kubectl_install_version }}/bin/linux/amd64/kubectl"
# Downloaded file name
kubectl_downloaded_file_name: kubectl
```

### Installation information

```yaml
# Path where to install terraform
kubectl_execution_path: /usr/local/bin
# Execution file name for terraform
kubectl_execution_file_name: kubectl
```

Dependencies
------------

No dependencie

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: ptavares.ansible_role_kubectl
```
Inside *`vars/main.yml`*:
- Copy content of [defaults/main.yml](https://github.com/ptavares/ansible-role-kubectl/blob/master/defaults/main.yml) in your playbook's vars file if needed.
- Customize it as you like (filling role's variables)

License
-------

MIT
