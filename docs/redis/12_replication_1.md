# Redis Replication

## What is replication

* 主从复制，就是主机数据更新后根据配置和策略，自动同步到备机的master/slave机制。Master以写为主，Slave以读为主。

## 用处

* 读写分离，性能扩展

* 容灾快速恢复

![](res/2021-01-08-20-20-24.png)

## Commands
* `info replication`

    show replication information

* `replicaof <ip> <port>`

    成为某个实例的从服务器


## 复制原理

* 每从机联通后′，都会给主机发送Sync命令

* 主机立刻进行存盘操作，发送RDB文件给从机

* 从机收到RDB文件后，进行全盘加载

* 之后每次主机的写操作，都会立刻发送给从机，从机执行相同的命令

![](res/2021-01-08-20-53-31.png)

## Chained Replica

* 上一个Slave可以是下一个Slave的Master。Slave同祥可以接收其他Slaves的连接和同步请求，那么该Slave作为链条中下一个的master， 可以有效减轻Master的压力，去中心化降低风险。

* 用`replicaof <ip> <port>`

* 中途变更转向，会清除数据，重新建立拷贝最新的。

* 风险是中间一个Slave down机，后续Slave无法拷贝

![](res/2021-01-08-21-01-31.png)
