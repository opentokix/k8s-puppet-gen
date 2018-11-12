# k8s-puppet-gen
Tool to autogenerate all puppetconfig for a k8s cluster

In the main block you configure your domain, if you use "hostname.domain.tld.yaml" as your config for your hiera lookups.

os is currently hardcoded to RHEL, will adjust that soonish and test for debuntu. 

Also only tested with flannel, docker - but it should work with others . :D 

**You need to run this on a host with a working docker installation, with a user that can run a docker container.**

```ini
[main]
domain = cloud.company.com
runtime = docker 
cniprovider = flannel 
os = rhel 
version = 1.10.2

[controllers]
master01 = 192.168.1.11
master02 = 192.168.1.12
master03 = 192.168.1.13

[workers]
worker01 = 192.168.1.21
worker02 = 192.168.1.22
worker03 = 192.168.1.23
worker04 = 192.168.1.24
worker05 = 192.168.1.25
worker06 = 192.168.1.26
worker07 = 192.168.1.27
worker08 = 192.168.1.28
```