# Infra and configuration code

[![Ubuntu 20.04 build](https://github.com/LexVar/infra/actions/workflows/ubuntu-20.04-build.yml/badge.svg)](https://github.com/LexVar/infra/actions/workflows/ubuntu-20.04-build.yml)

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
- ansible.cfg
- ssh, wireguard and prometheus roles - `example_play.yml`

### Tools
- ansible 2.9+
- python 3
- ansible-lint 5.1.2
- yamllint 1.26.2

## TODO
- [X] Include full ssh configuration
- [X] Setup proper folder structure with roles
- [X] SSH
	- [X] Custom sshd_config
	- [X] Firewall configuration
	- [X] Local key generation
- [X] Call firewall role
- [ ] Wireguard role
	- [X] Docker install
	- [X] Container 
	- [X] Firewall configuration
	- [ ] Add changed when to docker run
- [ ] Separate nginx role for config
- [ ] CI test pipeline with molecule
