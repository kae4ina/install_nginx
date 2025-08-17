configure nginx using ansible and open ports 22, 80, 443

### 1. create ssh-keys on control node
 ``` bash
ssh-keygen -t ed25519 -a 100
```

### 2. copy public key to managed nodes
 ``` bash
mkdir -p ~/.ssh
touch ~/.ssh/authorized_keys
chmod 700 ~/.ssh
chmod 600 ~/.ssh/authorized_keys
echo "key.pub" >> ~/.ssh/authorized_keys
```

### 3. run
 ``` bash
ansible-playbook nginx_fw_conf.yaml
 ``` 
