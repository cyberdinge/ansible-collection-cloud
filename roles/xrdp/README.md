# cyberdinge.xrdp

This will be the description of the role

## Requirements

a,b und c

## Defaults

``` YAML title="defaults/main.yaml"
--8<-- "./xrdp/defaults/main.yaml"
```


## change user passwords

Users must have a password set to be able to login via xrdp.
With ansible you can set the password of a linux user:

``` BASH
# ansible --become -m shell -a "echo <username>:<password> | chpasswd" all
ansible --become -m shell -a "echo testuser:testuserspassword | chpasswd" all
```