directories
===========

To create directories used to install Oracle Weblogic and Oracle SOA. Furthermore, this role is also used to populate some of these directories with binaries needed to install JDK, Weblogic, SOA, etc.

Requirements
------------

You need a Linux machine. In this example Centos 7 is used, but this can be adapted to be used with RedHat, Oracle Linux and any other suported Linux.

Role Variables
--------------
source_directory: /u01/software. Directory that contains the software this role will copy.

staging_directory: /u01/staging. Directory used to copy the SW from source_directory.

patch_directory: "{{ staging_directory }}/patches". Directory used to save patches.

soa_binaries['jdk8u251']['staging']. Directory used to save JDK package.

soa_binaries['jdk8u251']['installer_name']. File name used to copy the JDK package.

soa_binaries['weblogic12214']['staging']. Directory used to save Weblogic installer.

soa_binaries['weblogic12214']['installer_name']. File name used to copy the Weblogic installer.

soa_binaries['soa12214']['staging']. Directory used to save SOA installer.

soa_binaries['soa12214']['installer_name']. File name used to copy the SOA installer.

Dependencies
------------
This role depends on the variables declared at inventories/dev/group_vars/all.yml

Example Playbook
----------------

This roles can be executed as is shown below.

      - hosts: soa-admin:soa-managed
        remote_user: oracle
        tasks:
         - include_role:
            name: directories

License
-------

BSD

Author Information
------------------

[RSCC](https://www.linkedin.com/in/raul-castillo-11051980/)