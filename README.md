# Juniper Configuration Backups and VCS with Ansible
A quick example to show version control with network configuration backups.

Feel free to use the code where you wish.

## What's Required
In the hosts file, amend the host IP addresses and your username/ password for accessing your devices.
Not recommended to statically set your username/ password in the hosts file unless in a lab scenario, which I am. Otherwise; use an SSH key or Ansible Vault.
Ensure your current working directory is under git control.
Amend the git_control.yml file with your git username and repo as well as changing the paths to the configuration backup directory.
- Enable NETCONF on your devices
    - set system service netconf ssh

Ensure you have the correct Junos pip and Ansible galaxy packages installed:
- pip3 install junos-eznz
- pip3 install jxmlease
- pip3 install ansible
- ansible-galaxy install Juniper.junos

Blog post containing the basics: https://ducko.uk/ansible-juniper-configuration-and-vcs/