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

vim /etc/ssh/sshd_config
add **RSAAuthentication yes**
modify **PublicAuthentication yes**

if  you can login by the pub_keys 
then 
you can disable **PasswordAuthentication no**

finally 
```
systemctl restart sshd.service
```
or
```
service sshd restart
```


notices:

About the software using

1. Putty
> There is some notices on using the software.
> use the private_key must on ssh-auth windows choose the **ppk** file from  the browser.
> And connect the linux in the session 
2. Xshell
> this is simple , you can find the method by the graph windows
3. Juice
> this you must first to find the identify to fill your private_key up  &  give a name to the identify
> then choose the quick connect , fill the ip  and choose the identify that you alias just now
