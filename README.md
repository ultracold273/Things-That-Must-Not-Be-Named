# Things-That-Must-Not-Be-Named
It is a magic to jump across the great wall.

This tutorial is kept as a reminder of setting ladders on a remote server. 

## Prepare a remote server
There are a lot of choices aboard. A good reference is on [haoel's github page](https://haoel.github.io). A further note is that vps ips are consistently banned by the wall. It sometimes takes risk when you pay the price for remote servers if you cannot change ip afterwards. 

At this time point (2019-07-02), I've just bought an instance (KVM in Los Angeles) on [wikihost](https://idc.wiki) for around US$3.* per month.

## Setup your remote server
After your purchase, you find a control panel for your instance. Initially there are no operating system installed, you need to click on the Reinstall system button. Then you'll find a list of available systems. I chose the centos7 with tcp bbr. A few minutes later, the installation is done and then we can log in via ssh.

## Docker installation
Managing software with docker is a neat and convinient way. First we install the docker CE with instruction [here](https://docs.docker.com/install/linux/docker-ce/centos/).

Then we install the docker via the following command:
```bash
[root@remote]# docker run -dt --name ss -p [PORT]:[PORT] mritd/shadowsocks -s "-s 0.0.0.0 -p [PORT] -m chacha20-ietf-poly1305 -k [PASSWD] --fast-open
```

All is done. Connect to it with your local client.

Have fun
