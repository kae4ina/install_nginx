configure nginx using ansible and open ports 22, 80, 443
# 🔥 NGINX Configuration with Ansible

![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=for-the-badge&logo=ansible&logoColor=white)
![NGINX](https://img.shields.io/badge/NGINX-009639?style=for-the-badge&logo=nginx&logoColor=white)
![SSH](https://img.shields.io/badge/SSH-53A0D2?style=for-the-badge&logo=ssh&logoColor=white)

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
