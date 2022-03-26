ucf.ansible_role_httpd24_install
=========

Simple role that installs httpd24 on RHEL7/CentOS7/Amazon Linux 2

Requirements
------------

None.
  

Role Variables
--------------

httpd24_pkgs is a list of httpd packages to install:
```yaml
httpd24_pkgs:
  - httpd
```
Dictionary mapping of OS version and correlating repos containing desired httpd package(s).
```yaml
httpd24_repos:
  RedHatEnterpriseServer:
    '6': rhel-6-server-rpms
    '7': rhel-7-server-rpms
  CentOS:
    '6': base
    '7': base,updates
  Amazon:
    '2': amzn2-core
```
Dependencies
------------

Requires role: `ucf.ansible_role_lsb_core`

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```yaml
    - hosts: servers
      roles:
         - { ucf.ansible_role_httpd24_install }
```
License
-------

[MIT License](https://github.com/UCF/ansible-role-ucf.ansible_role_lsb_core/blob/master/LICENSE)

Author Information
------------------

Author(s): [Derek J. Bernard](https://github.com/derekjbernard), [Vinnie Vu](https://github.com/vinhtvu2)

