365-web common (Ansible pull)
===================

Requirements
------------

## Requirements - Almalinux 8

Install git, epel-release and ansible:

    sudo dnf install git epel-release -y && sudo dnf install ansible -y

Install Ansible collection ansible.posix:

    sudo ansible-galaxy collection install ansible.posix

Generating a new SSH key:

    ssh-keygen -t ed25519 && cat ~/.ssh/id_ed25519.pub

Test ssh connection:

    ssh git@github.com

Role Variables
--------------

Dependencies
------------

Example Playbook
----------------

Run deployment:

    ansible-pull -U git@github.com:myet3rnity/ansible_365-web_common.git -i hosts

After deployment, add management IPs:

    firewall-cmd --permanent --ipset=management --add-entry=1.2.3.4 && systemctl reload firewalld

License
-------
github:Myet3rnity
