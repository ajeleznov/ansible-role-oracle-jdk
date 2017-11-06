Role Name: ajeleznov.oracle-jdk
=========

Install the Oracle JDK, Java Platform Standard Edition Development Kit
on Redhat Family Linux (RedHat, CentOS) using RPM binary file

Requirements
------------

The target system is RPM-based Linux platform like Redhat or CentOs with x86_64 architecture.


Role Variables
--------------

See defaults/main.yml

Example Playbook
----------------

hosts:          test
gather_facts:   False

tasks:
- import_role:
    name: ajeleznov.oracle-jdk
  vars:
    delete_other_installations:   True
    java_version:                 "jdk1.8.0_131"
    workspace:                    "/tmp"

License
-------

BSD

Author Information
------------------

Dr. Andrei Jeleznov <mailto:andrei.jeleznov@kuehne-nagel.com>