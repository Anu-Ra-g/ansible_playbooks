# Ansible_playbooks

Resources gathered while learning Ansible. I'm using ansible from a virtual environment instead of installing it system wide. 


## Commands that I've used in the course:

1. `ansible all --key-file ~/.ssh/ansible -i inventory -m ping`
2. `ansible all --list-hosts`
3. `ansible all -m gather_facts`
4. `ansible all -m gather_facts --limit 192.168.0.118`