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

* do some test

```code
query consul service:

dig @127.0.0.1 consul-dc1.dalongrong.com

query public service:

dig @127.0.0.1 baidu.com
```