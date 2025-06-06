
# Redis

Redis (REmote DIctionary Server) is an open-source, in-memory data store used as a database, cache. It is known for ultra-fast performance due to its in-memory(stores in RAM) architecture. Uses a simple key-value model but supports complex data types.

**Versions of the DB Software you will get context from the developer, Meaning we need to check with developer.**

Install redis, By default redis 6 is available, We would like to enable 7 version and install list.

```shell 
dnf module disable redis -y
dnf module enable redis:7 -y
```

Install Redis 

```shell
dnf install redis -y 
```

Usually Redis opens the port only to `localhost(127.0.0.1)`, meaning this service can be accessed by the application that is hosted on this server only. However, we need to access this service to be accessed by another server, So we need to change the config accordingly.

Update listen address from `127.0.0.1` to `0.0.0.0` in   `/etc/redis/redis.conf`

Update `protected-mode` from `yes` to `no` in   `/etc/redis/redis.conf`

You can edit file by using **`vim /etc/redis/redis.conf`**

Start & Enable Redis Service 

```shell 
systemctl enable redis 
systemctl start redis 
```
