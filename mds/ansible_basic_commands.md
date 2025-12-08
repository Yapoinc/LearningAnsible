ansible all --key-file ~/.ssh/ansible -i inventory -m ping
ansible all -m ping
ansible all --list-hosts
ansible all -m gather_facts
ansible all -m gather_facts --limit bernardo@192.168.68.201
ansible all -m gather_facts --limit bernardo@192.168.68.201 | grep ansible_distribution

ansible all -m apt -a update_cache=true --become --ask-become-pass
ansible all -m apt -a name=vim-nox --become --ask-become-pass
ansible all -m apt -a name=tmux --become --ask-become-pass
ansible all -m apt -a name=snapd --become --ask-become-pass
ansible all -m apt -a "name=snapd state=latest" --become --ask-become-pass
ansible all -m apt -a "upgrade=dist" --become --ask-become-pass // sudo apt dist-upgrade


play playbook
--------------
ansible-playbook --ask-become-pass install_apache.yml
ansible-playbook --list-tags site.yml 
ansible-playbook --ask-become-pass  site.yml
ansible-playbook --ask-become-pass --tags centos  site.yml

ansible-playbook --ask-become-pass --tags "apache,db"  site.yml
ansible-playbook --ask-become-pass bootstrap.yml

