# How to use Inventory File

## How to use Inventory File
```
ansible-playbook -i <inventory> -l <host> <playbook.yml> --tags <tag_name>
```



## How to check Inventory
```
ansible-inventory  --graph
ansible-inventory -i INVENTORY --graph
```


```
$ ansible-inventory  --graph

@all:
  |--@production:
  |  |--@prd-group1:
  |  |  |--prd-server1
  |  |  |--prd-server2
  |--@stg-group1:
  |  |--stg-server1
  |  |--stg-server2
  |--@sub-group2:
  |  |--sub-server11
  |  |--sub-server12
  |--@ungrouped:
```


## How to check host
```
ansible-inventory  --host  DEVICE
ansible-inventory -i INVENTORY  --host  DEVICE
```
