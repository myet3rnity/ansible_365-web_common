# ansible_365-web_common

# Requirements - Almalinux 8

Install git and epel-release:

    sudo dnf install git epel-release -y
      
Install ansible:

    sudo dnf install ansible -y

Install Ansible collection ansible.posix:

    sudo ansible-galaxy collection install ansible.posix

Generating a new SSH key:

    ssh-keygen -t ed25519

Show public key:

    cat ~/.ssh/id_ed25519.pub

Test ssh connection:

    ssh git@github.com

# Deployment

Run deployment:

    ansible-pull -U git@github.com:myet3rnity/ansible_365-web_common.git -i hosts
