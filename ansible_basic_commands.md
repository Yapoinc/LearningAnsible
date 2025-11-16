ansible all --key-file ~/.ssh/ansible -i inventory -m ping
ansible all -m ping
ansible all --list-hosts
ansible all -m gather_facts
ansible all -m gather_facts --limit azureuser@4.228.56.51
