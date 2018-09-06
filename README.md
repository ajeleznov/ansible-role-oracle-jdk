Role Name: ajeleznov.oracle-jdk
=========

Install the Oracle JDK, Java Platform Standard Edition Development Kit
on Redhat Family Linux (RedHat, CentOS) using RPM binary file

You need to download JDK rpm files from Oracle site: http://www.oracle.com/technetwork/java/javase/downloads/index.html
and upload them into your local repository like Nexus OSS.
You need to specify an URL fo this repository (see Example Playbook) through parameter jdk_download_url.

This role will download the Oracle JDK rpm file from a local repository and
install it in the default location under /usr/java

Requirements
------------

The target system is RPM-based Linux platform like Redhat or CentOs with x86_64 architecture.


Role Variables
--------------

See defaults/main.yml

Example Playbook
----------------
```
hosts:		test
gather_facts:   False

tasks:
	- import_role:
	    name: ajeleznov.oracle-jdk
	  vars:
	    delete_other_installations:   True
	    java_version:                 "jdk1.8.0_151"
	    workspace:                    "/tmp"
      jdk_download_url:             "http://your-repository:8081/nexus/service/local/repositories/thirdparty/content/com/oracle/jdk/{{ jdk_version }}"
```

License
-------

BSD

Author Information
------------------

Dr. Andrei Jeleznov <mailto:andrei.jeleznov@kuehne-nagel.com>