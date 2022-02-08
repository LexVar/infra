# Server configuration code

This repo contains all my ansible configuration code for my home lab servers and workstation.

### Roles

- `ssh`: setups secure ssh configuration and with public key authentication
- `wireguard`: installs wireguard in docker container with nginx reverse proxy and downloads generated peer configs
- `adguardhome`: deploys local adguardhome
- `ansible-pull`: setups ansible-pull cron job which pulls and runs this playbook conf.
- `haproxy`: installs haproxy as a LB with a template configuration file
- `firewall`: setups simple firewalld/ufw
- `fedora`: personal workstation setup

Default variable values for each role, with examples, are present in each role's `defaults` folder.

### Playbooks

- `automatic-updates.yml`: enables automatic unattended updates for Debian/RedHat based linux
- `install-software.yml`: install packages and ansible dependencies

### Setup

The `requirements.yml` file contains all the necessary collections and role dependencies.

Dependencies can be installed by running (for ansible v2.9+):

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
