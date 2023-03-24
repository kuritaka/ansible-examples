# Ansible Examples with one yml file


## How to execute

```
$ ansible-playbook -i inventory_test.ini  test1.yml --syntax-check
$ ansible-playbook -i inventory_test.ini  test1.yml --check


$ ansible-playbook -i inventory_test.ini  test1.yml
$ ansible-playbook -i inventory_test.ini  test1.yml  --tags test1 --step
$ ansible-playbook -i inventory_test.ini  test1.yml  --tags test2 --step
```



