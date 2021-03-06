---
---

# FAQ

## 创建MySQL或者PostgreSQL的时候选的磁盘空间,没有让选数据副本,是单副本吗?

1. 不是单副本的;
2. 每个节点的数据, 默认都会维护多个实时副本数据;
3. 这些副本保存在不同的硬件上，可以确保某台硬件出现故障时，数据可以通过实时副本来恢复;
4. MySQL 或者 PostgreSQL 本身提供主从高可用机制, 底层数据也是多个副本去保证数据安全的.

## 如何创建\获取数据库超级权限的账户?

1. MySQL Plus 目前没提供超级权限root用户, 用户需要的话, 要提工单；
2. RDB-MySQL, RDB-PostgreSQL, App-PostgreSQL 在用户创建集群的时候, 就帮创建了超级权限的root用户, 密码和用户创建集群时指定的普通用户密码相同。

## RDB PostgreSQL 提供哪些服务？

1. RDB 提供PG 9.3, 9.4 服务。
2. 只提供一主一从的数据库服务

### RDB PostgreSQL 是否提供高可用读IP和高可用写IP？

不提供高可用读IP和高可用写IP

### 有哪些方式可以访问数据库？

只能通过主节点IP或者从节点IP来访问数据库。

### 从节点能写么？

主节点可以读写, 从节点只能读。

### 主从节点通过什么方式同步数据？

主节点和从节点通过异步复制的方式来同步数据。

### 主节点故障，从节点能自动切换么？

主节点故障，从节点不能自动切换，只能提供读服务。

### 提供读写分离Proxy节点么？

不提供读写分离Proxy节点。

### 是否具备可扩展性？

不具备可扩展性(增加节点)。

## APP PostgreSQL 提供哪些服务?

1. Appcenter 提供PG 9.6, 10 服务

2. 提供单节点和两节点集群服务
   
### 是否具备可扩展性？

暂时不具备可扩展性(增加节点)

### 提供读写分离Proxy节点么？

暂时不支持读写分离Proxy节点。

## APP PostgreSQL 是否提供高可用读IP和高可用写IP？

提供高可用写IP, 暂时不提供高可用读IP。

### 通过什么方式同步数据？

提供同步复制和异步复制方式，用户可以在控制台配置是否同步流复制。

### 是否支持故障自动切换？

支持故障自动切换, 用户可以在控制台配置是否开启AutoFailover功能。通过高可用写IP来访问, AutoFailover开启的话, 故障时会自动切换, 高可用写IP会漂移到新的主节点上并继续提供读写服务。

### 异步改成同步需要停业务吗？

不会影响业务, 业务感知不到.

### 改为同步模式后如果从节点宕机是否会影响主节点的读写？

1. 改为同步，从节点down了会影响主节点的写；
2. 从节点down了之后会有机制自动恢复服务，如果恢复不了，主节点只能读，无法写，集群会报异常，需要人工干预。