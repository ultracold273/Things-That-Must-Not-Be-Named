# Setting up V2ray

V2ray is a flexible proxy software from the scrutinizing of great wall.

To be continued.

```
$ sudo docker run -d --name v2ray -v /etc/v2ray:/etc/v2ray -p 51023:51023 v2ray/official v2ray -config=/etc/v2ray/config.json

$ sudo docker container start v2ray
$ sudo docker container stop v2ray
$ sudo docker container restart v2ray
$ sudo docker container logs v2ray
```
