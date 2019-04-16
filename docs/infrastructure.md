# Infrastructure

Goal: Looseleaf edge cloud infrasture setup, test, monitoring and useablity study.

## Network Map (internal)

| FQDN            | IP-LAN        | MAC               | dev     | HW            | Description |
| --------------- | ------------- | ----------------- | ------- | ------------- | ------------ |
| [xfirewall](http://192.168.1.1) | 192.168.1.1   | 1c:87:2c:c0:6e:50 | em0     | ASUS RT-N66R  | temp fw/router |
| [x freenas](http://192.168.1.2) | 192.168.1.2   | 00:15:17:4F:E7:7E | em0     | Dell SR1560SF | left RJ14 |
| [xxxxxxxxxxx]()                 | xxxxxxxxxxxx  | 00:15:17:4F:E7:7F | em1     | Dell SR1560SF | rght RJ14 not used |
| [gitlab.2cld.net](http://192.168.1.3) | 192.168.1.3   | 00:15:17:b1:cf:59 | epair0b | gitlab bsd jail   | virtural hw |
| [cfngnx.2cld.net](http://192.168.1.4) | 192.168.1.4   | 00:15:17:EE:CF:D6 | epair0b | cf-nginx bsd jail | virtural hw |
| [wip005.2cld.net](http://192.168.1.5) | 192.168.1.5   | 00:15:17:-------- | epair0b | TBD--------jail   | virtural hw |
| [plex.2cld.net](http://192.168.1.6)   | 192.168.1.6   | 00:15:17:14:FA:0A | epair0b | plex bsd jail     | virtural hw |
| ----------------- | 192.168.1.x   | 00:15:17:b1:cf:xx | epair0b | vm bsd jail   | virtural hw |
| -- DHCP Start   | 192.168.1.20  | ----------------- | ------- | ------------- | ---- |
| -- DHCP End     | 192.168.1.199 | ----------------- | ------- | ------------- | ---- |

## Task

| Task            | Goal | Status  |
| --------------- | ------------------------------------------------------ | -------- |
| Setup FreeNAS   | User storage access [lls-FreeNAS Setup](lls-FreeNAS.md) document | WIP-Works but needs doc |
| Setup gitLab    | User access [lls-gitLab Setup](lls-gitLab.md) document  | WIP-Works but needs doc |
| Setup firewall  | Remote access by User [lls-firewall Setup](lls-firewall.md) document. | WIP-Works but needs doc |
| proxmox cluster | Remote access by User [lls-proxmox Setup](lls-proxmox.md) document. | WIP-Works but needs doc |
| nginx proxy     | https access by User [lls-nginx Setup](lls-nginx.md) document.  | WIP-Works but needs doc |
| deploy Test     | One button deploy and validate [lls-nodejs-test](lls-nodejs-test.md) document. | no progress |
| load Test     | One button load test [lls-nodejs-load](lls-nodejs-load.md) document. | no progress |
| dr Test       | Test digital rebar | no progress |
| bm node add | Test a bare metal node add | no progress |
| dr package matrix test | tbd | tbd |
| k8s project | Test a k8s project | np |
| ceph testing | Test using ceph on C7000 nodes | np |

## Infrastructure Diagram

![lls-infrastructure-diagram svg](images/lls-infrastructure-diagram.svg)

Source edit [lls-infrastructure-diagram draw.io](https://www.draw.io/#Hlooseleaf%2Flls-nodejs-test%2Fmaster%2Fdocs%2Fimages%2Flls-infrastructure-diagram.drawio


### Server H/W

| Device | Description | Link |
| ----------- | ---------------- | --------- |
| cfx grid node  | CPU HB           | [cpu Xeon E3-1230](https://ark.intel.com/content/www/us/en/ark/products/97474/intel-xeon-processor-e3-1230-v6-8m-cache-3-50-ghz.html) |
| FreeNAS  | CPU CF           | [cpu Xeon E5462](https://ark.intel.com/content/www/us/en/ark/products/33084/intel-xeon-processor-e5462-12m-cache-2-80-ghz-1600-mhz-fsb.html) |

### Notes

1. [NGINX Reverse Proxy](https://www.nginx.com/resources/glossary/reverse-proxy-server/)
2. [gitlab CI/CD Tutorial](https://medium.com/devopslinks/beginner-friendly-introduction-to-gitlab-ci-cd-1c80ee5ba0ae)
3. [gitlab nodejs app deploy](https://medium.com/@seulkiro/deploy-node-js-app-with-gitlab-ci-cd-214d12bfeeb5)
4. [gitlab examples](https://gitlab.com/gitlab-examples)
5. [gitlab CI/CD](https://about.gitlab.com/2016/03/01/gitlab-runner-with-docker/)
6. [gitlab nginx https docker how-to](https://www.digitalocean.com/community/tutorials/how-to-secure-a-containerized-node-js-application-with-nginx-let-s-encrypt-and-docker-compose)
7. [gitlab autodevops](https://docs.gitlab.com/ee/topics/autodevops/#auto-monitoring)

[markdown cheat sheet](http://blog.christrees.com/wip/markdowntest.html)
