# Ansible_playbooks

Resources gathered while learning Ansible. I'm using ansible from a virtual environment instead of installing it system wide. 


## Commands that I've used in the course:

1. `ansible all --key-file ~/.ssh/ansible -i inventory -m ping`
2. `ansible all --list-hosts`
3. `ansible all -m gather_facts`
4. `ansible all -m gather_facts --limit 192.168.0.118` (to limit the host options)
5. `ansible all -m apt -a update_cache=true` (without sudo privilieges)
6. `ansible all -m apt -a update_cache=true --become --ask-become-pass` (--ask-become-pass if you don’t have passwordless sudo set up)
7. `ansible  all -m apt -a name=openvpn --become --ask-become-pass`
8. `ansible all -m apt -a "name=dpkg state=latest" --become --ask-become-pass` (upgrade a package in the target node)
9. `ansible all -m apt -a "upgrade=dist" --become --ask-become-pass` (to install all the package updates)
10. `ansible-playbook --ask-become-pass playbooks/install_apache.yml` (running a playbook with path to it)