SSH
=========

Installs and hardens configuration of ssh server.

Requirements
------------

Role Variables
--------------

Some variables can be set:
- `ssh_user` - remote previliged user allowed to log in
- `private_key` - local private key to be loaded
- `ssh_port` - ssh server port

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------
```
    - hosts: ssh_hosts
      roles:
         - ssh
	   vars:
	     ssh_user: 'admin'
	     private_key: "/home/admin/.ssh/ssh_key"
	     ssh_port: '22'
```

License
-------

MIT

Author Information
------------------
