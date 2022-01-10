# Server configuration code

This repo contains all my ansible configuration code for my home lab servers and workstation.

### Roles

- Fedora workstation setup role
- SSH: secure server configuration with public key authentication
- Wireguard: installs wireguard in docker container with nginx reverse proxy and downloads generated peer configs (qrcodes).
- HAProxy: installs haproxy with a template configuration file
- [Prometheus ansible role](https://github.com/LexVar/ansible-prometheus)

### Playbooks

- `firewall.yml`: setups simple firewalld or ufw with tcp and udp open ports
- `automatic-updates.yml`: enables automatic unattended updates for Debian and RedHat

### Setup

The `requirements.yml` file contains all the necessary collections and role dependencies.

Dependencies can be installed by running (for ansible v2.9+):

	ansible-galaxy install -r requirements.yml
	ansible-galaxy collection install -r requirements.yml

### Usage Examples

This repo contains example files for using these roles:
- `server.yml`
- `ansible.cfg`
- fedora workstation setup - `fedora.yml`

### Tools
- ansible 2.9+
- python 3

## TODO

- [ ] Fedora Workstation role
	- [ ] Fix dotfiles git pull
	- [ ] Add ~/.bin links to /usr/local/bin/
