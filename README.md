Role Name
=========

Install Redmine on RedHat / CentOS 7, Debian Jessie, or Gentoo

Requirements
------------

When hiawatha or lighttpd is selected as web server, the packages needed to run it with fcgi support should be installed ahead of time. This role does not currently install those packages. Note that hiawatha is not available in official repos for RedHat or Debia.

Role Variables
--------------

* redmine_version
* redmine_topdir
* redmine_appdir
* redmine_staticdir
* sql_database_type
* sql_database_name
* sql_database_host
* sql_username
* sql_password
* app_server_type
* web_server_type
* web_server_hostname
* web_server_ip
* web_server_port
* firewall_type

Dependencies
------------

No other dependencies.


Example Playbook
----------------

Example playbook

    - hosts: servers
      remote_user: root
      roles:
         - { role: redmine, sql_username: redmine, sql_password: password, sql_database_name: redmine, sql_database_host: localhost, redmine_version: 3.2.1, app_server_type: uwsgi, web_server_type: uwsgi, firewall_type: firewalld }

License
-------

BSD

Author Information
------------------

S. Lockwood-Childs
based on bngsudheer.redmine role by Sudheer Satyanarayana
