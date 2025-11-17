ansible all --key-file ~/.ssh/ansible -i inventory -m ping
ansible all -m ping
ansible all --list-hosts
ansible all -m gather_facts
ansible all -m gather_facts --limit bernardo@192.168.68.201

ansible all -m apt -a update_cache=true --become --ask-become-pass
ansible all -m apt -a name=vim-nox --become --ask-become-pass
ansible all -m apt -a name=tmux --become --ask-become-pass
ansible all -m apt -a name=snapd --become --ask-become-pass
ansible all -m apt -a "name=snapd state=latest" --become --ask-become-pass
ansible all -m apt -a "upgrade=dist" --become --ask-become-pass // sudo apt dist-upgrade
