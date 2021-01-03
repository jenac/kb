# Redis configuration file

## redis.conf
* docker image: docker.io/bitnami/redis:latest, location: /opt/bitnami/redis/etc/redis.conf
* `tcp-backlog` depends on /proc/sys/net/core/somaxconn, need set both.
* `maxmemory-policy: MAXMEMORY POLICY, how Redis will select what to remove when maxmemory is reached. You can select one from the following behaviors:
    * volatile-lru -> Evict using approximated LRU, only keys with an expire set.
    * allkeys-lru -> Evict any key using approximated LRU.
    * volatile-lfu -> Evict using approximated LFU, only keys with an expire set.
    * allkeys-lfu -> Evict any key using approximated LFU.
    * volatile-random -> Remove a random key having an expire set.
    * allkeys-random -> Remove a random key, any key.
    * volatile-ttl -> Remove the key with the nearest expire time (minor TTL)
    * noeviction -> Don't evict anything, just return an error on write operations.
        * LRU means Least Recently Used
        * LFU means Least Frequently Used
        * Both LRU, LFU and volatile-ttl are implemented using approximated randomized algorithms.

