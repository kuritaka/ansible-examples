# Ansible Examples



## How to check without Ansible Playbook
### How to check ansible's environment
```
ansible --version
ansible-config dump --only-changed
```


### How to check inventory

```
ansible-inventory  --graph
ansible-inventory  --host  DEVICE
```


## How to check Ansible Playbook

### How to check Ansible Playbook's Syntax Check

```
nsible-playbook xxxx.yml --syntax-check
```

### How to check the hosts to be executed
```
ansible-playbook  playbooks/test1.yml --list-hosts
```

### How to check the task to be executed
```
ansible-playbook  playbooks/test1.yml --list-tasks
```

### Dry Run
```
ansible-playbook  -l <host> playbooks/<playbook.yml>  -C --diff
ansible-playbook  -l <host> playbooks/<playbook.yml>  --check --diff

ansible-playbook  -l <host> playbooks/<playbook.yml>  -C
ansible-playbook  -l <host> playbooks/<playbook.yml>  --check
```

### Execute
```
ansible-playbook -l <host> playbooks/<playbook.yml>
ansible-playbook -l <host> playbooks/<playbook.yml> --tags <tag_name>

ansible-playbook -v -l <host> playbooks/<playbook.yml>
```


## How to execute ansible-playbook
```
ansible-playbook  playbooks/test1.yml --check           # Execute Test


ansible-playbook  playbooks/test1.yml
or
ansible-playbook  -l test1  playbooks/test1.yml
```

