# Git

### Install Git

```bash
sudo apt install git -y

# or
 
sudo yum install git -y
```

### Git config

```bash
git config --global user.name "Tan"
git config --global user.email duytan4work@gmail.com
```

```bash
git config user.name "Tan"
git config user.email duytan4work@gmail.com
```

### SSH generate key pair

```bash
ssh-keygen -t ed25519 -C "duytan4work@gmail.com"
```

```bash
ssh-keygen -t rsa -b 4096 -C "duytan4work@gmail.com"
```

### SSH Config

```bash
nano ~/.ssh/config
```

```bash
Host team1.github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/key1.pem
 
Host team2.github.com
  HostName github.com
  User git
  IdentityFile ~/.ssh/key2.pem
```

```bash
git clone git@github.com:dev2am/cms-next.git

# or

git clone git@team1.github.com:dev2am/cms-next.git

git clone git@team2.github.com:dev2am/cms-next.git
```