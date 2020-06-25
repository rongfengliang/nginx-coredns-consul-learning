# nginx coredns lb + consul

> use coredns rewrite、forward、loadbalance plugin

## Hwo to Running

* touch  log file

```code

touch dns.log
```

* start service

```code
docker-compose up -d
```
* add one service

```code
curl -X PUT -d '{"ID": "openresty","Name": "openresty","Address": "192.168.1.2","Port": 80}' http://127.0.0.1:8500/v1/agent/service/register
```

* do some test

```code
query consul service:

dig @127.0.0.1 openresty-dc1.dalongrong.com

query public service:

dig @127.0.0.1 baidu.com
```