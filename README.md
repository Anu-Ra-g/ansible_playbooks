# Ansible_playbooks

Resources gathered while learning Ansible. I'm using ansible from a virtual environment using `pip` instead of installing it system wide. 


## Commands that I've used in the course:

1. `ansible all --key-file ~/.ssh/ansible -i inventory -m ping` (specified the path to public key if not in configuration)
2. `ansible all --list-hosts`
3. `ansible all -m gather_facts` (here we're not playing any playbook)
4. `ansible all -m gather_facts --limit 192.168.0.118` (to limit the host options)
5. `ansible all -m apt -a update_cache=true` (without sudo privilieges)
6. `ansible all -m apt -a update_cache=true --become --ask-become-pass` (--ask-become-pass if you don’t have passwordless sudo set up and --become to use sudo)
7. `ansible  all -m apt -a name=openvpn --become --ask-become-pass`
8. `ansible all -m apt -a "name=dpkg state=latest" --become --ask-become-pass` (upgrade a package in the target node)
9. `ansible all -m apt -a "upgrade=dist" --become --ask-become-pass` (to install all the package updates)
10. `ansible-playbook --ask-become-pass playbooks/install_apache.yml` (running a playbook with path to it)
11. `ansible-playbook --list-tags server_groups.yml` (lists the tags mentioned in the plays)
12. `ansible-playbook --tags centos --ask-become-pass server_group.yml` (only run the plays with the mentioned tags which is "centos" in this case)
13. `ansible-playbook --tags "apache,db" --ask-become-pass server_group.yml` (only run plays with the tags mentioned)
14. 

## Notes:
> `gather_facts` is a default task that runs at the start of every play, unless you explicitly disable it.`
> Ansible playbooks are idempotent i.e. running a playbook multiple times will not change the state of the managed servers