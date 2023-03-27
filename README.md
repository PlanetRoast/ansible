PlanetRoast Ansible Playbooks
================================================================================

1. Install ansible

You'll need to add the Ansible PPA to get the latest version in order for the
playbook to run as the version that comes with Mint is too old and you'll get an
error when running some of the roles.

```
sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository --yes ppa:ansible/ansible
sudo apt update
sudo apt install ansible
```

2. Run the playbook

```
ansible-playbook build-desktop.yml --ask-become-pass
```

The `--ask-become-pass` option will prompt you for your password before things
kick off. This is necessary because some of the roles require sudo such as
installing packages etc.

