# lls infrastructure setup

Attempt to document infrastructure

| Link | Description |
| ----------- | ----------- |
| [gitlab looseleaf](https://gitlab.com/looseleaf) | gitlab looseleaf group |
| [github lls-nodejs-test](https://github.com/looseleaf/lls-nodejs-test) | github lls-nodejs-test project |
| [lls-infrastructure-diagram draw.io](https://www.draw.io/#Hlooseleaf%2Flls-nodejs-test%2Fmaster%2Fdocs%2Fimages%2Flls-infrastructure-diagram.drawio) | lls-infrastructure-diagram via draw.io |

## Infrastructure Diagram

![lls-infrastructure-diagram svg](images/lls-infrastructure-diagram.svg)

Source edit [lls-infrastructure-diagram draw.io](https://www.draw.io/#Hlooseleaf%2Flls-nodejs-test%2Fmaster%2Fdocs%2Fimages%2Flls-infrastructure-diagram.drawio)

### Server H/W

| Device | Description | Link |
| ----------- | ---------------- | --------- |
| FreeNAS HB  | CPU HB           | [cpu Xeon E3-1230](https://ark.intel.com/content/www/us/en/ark/products/97474/intel-xeon-processor-e3-1230-v6-8m-cache-3-50-ghz.html) |
| FreeNAS HB  | CPU CF           | [cpu Xeon E5462](https://ark.intel.com/content/www/us/en/ark/products/33084/intel-xeon-processor-e5462-12m-cache-2-80-ghz-1600-mhz-fsb.html) |

### Notes

[NGINX Reverse Proxy](https://www.nginx.com/resources/glossary/reverse-proxy-server/)
