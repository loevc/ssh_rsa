1. generate key 
```
ssh-keygen -C "loevc@github" -t rsa -f id_rsa_github
```
![generate key](IMAGE/Screenshot%20from%202021-01-27%2014-43-18.png)

2. add the public key to the github  
```
cat id_rsa_github.pub
```
![02](IMAGE/Screenshot from 2021-01-27 14-46-52.png)

**copy the public_key to the github's setting ssh .**

3. ssh-add
```
ssh-add id_rsa_github
```
![03](IMAGE/Screenshot from 2021-01-27 14-43-40.png)

4. identify the tunnel
```
ssh -T git@github.com
```

5. use once passwd then will not again (if you band the ssh)


