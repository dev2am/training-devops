# SSH, SCP

### SSH connect

```bash
ssh -i /path/key-pair-name.pem ec2-user@ip-address -p 22
ssh -i /path/key-pair-name.pem ec2-user@public-dns -p 22
```

### SSH generate key pair

```bash
ssh-keygen -t ed25519 -C "duytan4work@gmail.com"
```

```bash
ssh-keygen -t rsa -b 4096 -C "duytan4work@gmail.com"
```

```bash
sudo nano /etc/ssh/sshd_config
```

```bash

PubkeyAuthentication yes

PasswordAuthentication no

```

```bash
sudo systemctl restart ssh
```

### SSH Config

```bash
nano ~/.ssh/config
```

```bash
Host myec2dns
    HostName ec2-3-21-21-21.us-west-2.compute.amazonaws.com
    User ec2-user
    IdentityFile ~/.ssh/my-key.pem

Host myec2ip
    HostName 3.21.21.21
    User ec2-user
    IdentityFile ~/.ssh/my-key.pem
```

```bash
ssh myec2dns
ssh myec2ip
```

### SCP transfer files
```bash
scp -i /path/key-pair-name.pem ec2-user@ip-address:/home/ec2/ec2.txt ./ec2.txt
scp -i /path/key-pair-name.pem ./mac.txt ec2-user@ip-address:/home/ec2/mac.txt

#copy folder
scp -i /path/key-pair-name.pem -r ./mac ec2-user@ip-address:/home/ec2/

```

### SSH client tools 
- https://termius.com/