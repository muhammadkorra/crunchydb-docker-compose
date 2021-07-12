# Minimal Crunchy PostgreSQL setup for Dev Environment

Provide a minimal HA PostgreSQL Development environment for developers to test their code with replicated PostgreSQL.

> This is not an Optimal setup for Production environments. You may need to do a little bit of tweaking.

Crunchy PostgreSQL leverages built-in __Streaming Replication__ to keep the Primary and Standby Node In-sync. 
PGPool-II acts as a Load Balancer for __READ__ queries (Sent to both nodes) and __WRITE/UPDATE/DELETE__ queries are sent to the primary node.

## Requirements
- docker-compose

## RUN

```shell
$ sudo chmod +x start.sh
$ ./start.sh
```

## Takedown

```shell
$ sudo chmod +x cleanup.sh
$ ./cleanup.sh
```