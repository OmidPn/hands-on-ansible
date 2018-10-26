Role Name
=========

Installs PM2 as service on top of NodeJS

Requirements
------------

NodeJs must be installed

Role Variables
--------------

pm2_service_name: The name that will be listed when looking at the running services on your system
pm2_user: pm2 user, must be an existing user on your machine
pm2_version: pm2 version to install
pm2_service_state: state in which you want pm2 after the script ran

Dependencies
------------

none

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: pm2-service-installation }

License
-------

Private to Sogema Technologies

Author Information
------------------
