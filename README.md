#Starting Ansible with Junos

## Follow the below steps to setup your first ansible play book

```
1. create an ansible.cfg file 
2. create an inventory/hosts file
3. create a playbook < >.yaml file
```

### ansible.cfg 
```
vim ansible.cfg

[defaults]
inventory = hosts
host_key_checking = False
```

### hosts
```
vim hosts

99.99.99.5 junos_host=99.99.99.5

we can also mention fully resolved name
groups can be added using the format

[vmx]
99.99.99.5
99.99.99.6
99.99.99.7
```

### Playbooks
refer the sample scripts

### Run the playbook 
ansible-playbook < >.yaml -u <username> --ask-pass 

if you plan on using inventory file which is on another directory  
ansible-playbook < >.yaml -i <inventory file > -u <username> --ask-pass

