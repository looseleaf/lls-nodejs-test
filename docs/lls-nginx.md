# lls nginx setup

Goal: Looseleaf https remote access to web portals.

## Task

| Task            | Goal | Status  |
| --------------- | ------------------------------------------------------ | -------- |
| nginx - FreeNAS | nginx on FreeNAS installation. | WIP |
| letsencrypt     | Add letsencrypt | no progress |
| ci/cd test | ci/cd workflow in gitlab | no progress |
| co | co dashboard | no progress |


### Services

| Service | Description | Link |
| ----------- | ---------------- | --------- |
| firewall | firewall admin | [http://192.168.1.1](http://192.168.1.1) |
| httpd | nginx    |  |
| SOA | SOA for 2cld.net | [Google Domains](https://domains.google.com)

### Notes

- [NGINX.com](https://www.nginx.com/)
- [letsencrypt.org](https://letsencrypt.org/)
- [NGINX Lets Encrypt with certbot](https://www.nginx.com/blog/using-free-ssltls-certificates-from-lets-encrypt-with-nginx/)
- [nginx-letsencrypt-freebs](https://www.digitalocean.com/community/tutorials/how-to-secure-nginx-letsencrypt-freebsd)
- [nginx-freebsd-11-2](https://www.digitalocean.com/community/tutorials/how-to-install-nginx-freebsd-11-2)

[markdown cheat sheet](http://blog.christrees.com/wip/markdowntest.html)# lls nginx setup

## Install Notes

1. Login to [x freenas](http://192.168.1.2)
2. create cf-nginx
3. mount source: cf-nginx to destination: media

```
root@cf-nginx:~ # history
     1  13:35   ifconfig
     2  13:36   ping 192.168.1.1
     3  13:36   ifconfig
     4  13:39   ifconfig
     5  13:48   ping 192.168.1.1
     6  13:48   ls
     7  13:48   pwd
     8  14:49   sudo pkg install nginx
     9  14:49   pkg install nginx
    10  14:50   rehash
    11  14:50   echo $SHELL
    12  14:51   grep rcvar /usr/local/etc/rc.d/*
    13  14:52   vi /etc/rc.conf
    14  14:55   vi /etc/rc.conf
    15  15:00   nohup service ipfw start > & /tmp/ipfw.log
    16  15:00   service service nginx start
    17  15:01   source /etc/rc.conf
    18  15:01   src /etc/rc.conf
    19  15:02   sudo service nginx
    20  15:02   service nginx
    21  15:02   service nginx start
    22  15:09   history
root@cf-nginx:~ #
```

