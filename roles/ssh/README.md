SSH
=========

Installs and hardens configuration of ssh server.

Requirements
------------

Role Variables
--------------

Some variables can be set:
- `ssh_user` and `ssh_group` - remote user and group allowed to be logged in
- `public_key` - path for the local public key which will be loaded to the servers
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
	     ssh_user: 'avalente'
	     ssh_group: 'avalente'
	     ssh_group: "/home/user/.ssh/ssh_key.pub"
	     ssh_port: '22'
```

License
-------

MIT

Author Information
------------------
