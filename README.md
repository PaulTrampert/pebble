Role Name
=========

Runs a pebble ACME server for testing playbooks that include the nginx-proxy role. Exposes pebble on localhost:14000

Requirements
------------

None.

Role Variables
--------------

None

Dependencies
------------

git+http://github.com/PaulTrampert/ansible-docker.git

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      become: true
      roles:
         - pebble

License
-------

MIT
