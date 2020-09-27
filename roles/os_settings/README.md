os_settings
===========

The goal of this role is to set the Linux (CentOS 7) Operating System according to the requirements provided by Oracle to install an Oracle Fusion Middleware 12.2.1.4

Importantly, I do not think Centos is supported by Oracle. However, this is just a development environment so I have used the list of OS packages that Oracle recommends for RedHat 7 and Oracle Linux 7.

Requirements
------------

You need a machine with Centos 7 and do not forget to execute this.

Role Variables
--------------
os_packages, a list of OS packages installed on target(s) machines.

limits, a dictionary, which represents the soft and hard limits for processes and files to be set before installing Oracle database.

Dependencies
------------
At this moment this roles does not depend on other roles or external variables.

Example Playbook
----------------

This roles can be executed as is shown below.

      - hosts: soa-admin:soa-managed
        remote_user: oracle
        tasks:
         - include_role:
            name: os_settings

License
-------

BSD

Author Information
------------------

[RSCC](https://www.linkedin.com/in/raul-castillo-11051980/)