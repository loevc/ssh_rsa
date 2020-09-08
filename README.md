# ssh_rsa

use the rsa to login 
environment 
> centos7.7 

```
ssh-keygrn
```
to do follow the tips  &  enter a passphrase

will generate two files
the one is the pbulic key **id_rsa.pub**
the other is the private key **id_rsa**

```
cd /root/.ssh
cat id_rsa.pub >> authorized_keys
```

this op complete the skips of installing rsa

then , you need use the permission to grant
```
chmod 600 authorized_keys
chmod 700 ~/.ssh
```

edit /etc/ssh/sshd_config
add **RSAAut
