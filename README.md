# Infra and configuration code

This repo contains all my infrastructure and configuration code for my home lab.

### Roles
- SSH: secure server configuration with public key authentication
- Wireguard: installs wireguard in docker container with nginx reverse proxy, downloads peer configs.
	- This configuration was tested on a raspberry pi 3B and orange pi zero
- [Prometheus ansible role](https://github.com/LexVar/ansible-prometheus)

### Setup

The `requirements.yml` file contains all the necessary collections and role dependencies.

All dependencies can be installed by running (ansible v2.9+ is necessary):
```
ansible-galaxy install -r requirements.yml && ansible-galaxy collection install -r requirements.yml
```

### Usage Examples

This repo contains example files for using these roles:
- inventory.ini
- ansible.cfg
- ssh and wireguard roles - `example_play.yml`
- prometheus role - `example_prometheus.yml`

### Tools
- ansible 2.9+
- python 3

## TODO
- [X] Include full ssh configuration
- [X] Setup proper folder structure with roles
- [X] SSH
	- [X] Custom sshd_config
	- [X] Firewall configuration
	- [ ] Local key generation with tag
- [X] Wireguard role
	- [X] Docker install
	- [X] Container 
	- [X] Firewall configuration
- [ ] CI test pipeline
