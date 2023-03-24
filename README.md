# Ansible Examples

<br>
This is my Ansbile best practices
<br>
<br>


## How to install Ansible
### Ubuntu 22.04(WSL)

```
$ sudo apt-get update
$ sudo apt-get install ansible
$ sudo apt install sshpass
$ ansible --version

# For WSL
$ export ANSIBLE_CONFIG=$(pwd)
```

<br>

## Server Configuration

### Target Server

```
# useradd ansible
# echo 'ansible:ansible' | chpasswd

# vi /etc/ssh/sshd_config
PasswordAuthentication yes

# systemctl reload sshd.service


# cp -p  /etc/sudoers  /etc/sudoers.`date -d '1day ago' +%Y%m%d`
# visudo
ansible    ALL=(ALL)   NOPASSWD:ALL
```


### Manager Server

```
$ ssh-keygen -t rsa -b 2048 -C "ansible"  -N "" -f "ansible"
$ ssh-copy-id -i ansible  ansible@${target_host}
```

