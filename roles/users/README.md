# cyberdinge.users

Manages linux users 

- adds or deletes users
- manages sudo permissions

## Requirements


``` YAML title="vars/users.yaml"
users:
  
  # User can login and is able to sudo
  - name: eampleuser0
    state: present
    sudoer: true
    key: <ssh key>
    wireguard_address: 172.0.90.240
    wireguard_public_key: WTmaW1Zhe3253554wmN43MBRveToQEZ+bZHWs=

  # User can login but is not able to sudo
  - name: eampleuser1
    state: present
    sudoer: false
    key: <ssh key>
    wireguard_address: 172.0.1.241
    wireguard_public_key: VLMvIqVYbCSD4Gdfe53Zz5hJv9j2RU4ABwvlc=

  # User is removed from the host
  - name: eampleuser2
    state: absent
```