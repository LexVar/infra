# Ansible configuration repo

### Roles
- SSH: secure server configuration with public key authentication
- Wireguard: installs wireguard in docker container with nginx reverse proxy, downloads peer configs.

### Setup
```
ansible-galaxy collection install community.general
ansible-galaxy collection install ansible.posix
```

### Tools
- ansible 2.9.18
- python 3.9.2

## TODO
- [X] Include full ssh configuration
- [X] Setup proper folder structure with roles
- [X] Wireguard role
	- [X] Docker install
	- [X] Container 
	- [X] Firewall configuration
