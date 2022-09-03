# Redis Hands On

## Start on docker

```bash
docker run --name redis -d redis
```

```bash
docker exec -it redis bash
```

## Start redis cli

Note: run this command inside redis container.

```bash
redis-cli
```

## Commands

### Print message

```bash
ECHO "MY_MESSAGE"
```

### Set value

```bash
SET "MY_KEY" "MY_VALUE"
```

### Set multiple values

```bash
MSET "MY_KEY_1" "MY_VALUE_1" "MY_KEY_2" "MY_VALUE_2" "MY_KEY_3" "MY_VALUE_3"
```

### Get value

```bash
GET "MY_KEY"
```

### Delete value

```bash
DEL "MY_KEY"
```

### Get all keys

```bash
KEYS *
```

### Search key

```bash
KEYS "MY_KEY_PART"
```

### Set value in hash

```bash
HSET "MY_KEY" "MY_HASH_KEY" "MY_VALUE"
```

### Set multiple values in hash

```bash
HSET "MY_KEY" "MY_HASH_KEY_1" "MY_VALUE_1" "MY_HASH_KEY_2" "MY_VALUE_2" "MY_HASH_KEY_3" "MY_VALUE_3"
```

### Get value in hash

```bash
HGET "MY_KEY" "MY_HASH_KEY"
```

### Get all values in hash

```bash
HGETALL "MY_KEY"
```

### Delete value in hash

```bash
HDEL "MY_KEY" "MY_HASH_KEY"
```

### Set expire time

```bash
EXPIRE "MY_KEY" TIME_IN_SECONDS
```

### Get time left

```bash
TTL "MY_KEY"
```

### Increment value

```bash
INCR "MY_KEY"
```

### Increment integer values

```bash
INCRBY "MY_KEY" INCREMENT_VALUE
```

### Increment float values

```bash
INCRBYFLOAT "MY_KEY" INCREMENT_VALUE
```

### Increment integer value in hash

```bash
HINCRBY "MY_KEY" "MY_HASH_KEY" INCREMENT_VALUE
```

### Increment float value in hash

```bash
HINCRBYFLOAT "MY_KEY" "MY_HASH_KEY" INCREMENT_VALUE
```

### Decrement value

```bash
DECR "MY_KEY"
```

### Decrement integer values

```bash
DECRBY "MY_KEY" DECREMENT_VALUE
```

### Decrement float values

```bash
DECRBYFLOAT "MY_KEY" DECREMENT_VALUE
```

### Decrement integer value in hash

```bash
HDECRBY "MY_KEY" "MY_HASH_KEY" DECREMENT_VALUE
```

### Decrement float values in hash

```bash
DECRBYFLOAT "MY_KEY" "MY_HASH_KEY" DECREMENT_VALUE
```

### Set bit value

```bash
SETBIT "MY_KEY" OFFSET 0/1
```

### Get bit value

```bash
GETBIT "MY_KEY" OFFSET
```

### Count bit values

```bash
BITCOUNT "MY_KEY"
```

### AND operation

```bash
BITOP AND "MY_NEW_KEY" "MY_KEY_1" "MY_KEY_2"
```

### OR operation

```bash
BITOP OR "MY_NEW_KEY" "MY_KEY_1" "MY_KEY_2"
```

### Add element to list on the left

```bash
LPUSH "MY_KEY" "MY_VALUE"
```

### Add element to list on the right

```bash
RPUSH "MY_KEY" "MY_VALUE"
```

### Remove elements from a list while keeping a sublist

```bash
LTRIM "MY_KEY" SUBLIST_START_INDEX SUBLIST_END_INDEX
```

### Get element from list by index

```bash
LINDEX "MY_KEY" MY_INDEX
```

### Get list length

```bash
LLEN "MY_KEY"
```

### Get sublist from a list

```bash
LRANGE "MY_KEY" SUBLIST_START_INDEX SUBLIST_END_INDEX
```

### Get and remove first element from a list

```bash
LPOP "MY_KEY"
```

### Get and remove last element from a list

```bash
RPOP "MY_KEY"
```

### Get and remove first element from a list (block until have any data)

```bash
BLPOP "MY_KEY" TIMEOUT (0 for infinity)
```

### Get and remove last element from a list (block until have any data)

```bash
BRPOP "MY_KEY" TIMEOUT (0 for infinity)
```

### Add element to a set

```bash
SADD "MY_KEY" "MY_VALUE_1" "MY_VALUE_2"
```

### Get set cardinality

```bash
SCARD "MY_KEY"
```

### Get set cardinality

```bash
SMEMBERS "MY_KEY"
```

### Check if value is member of a set

```bash
SISMEMBER "MY_KEY" "MY_VALUE"
```

### Remove member of a set

```bash
SREM "MY_KEY" "MY_VALUE"
```

### Get intersection between two sets

```bash
SINTER "MY_KEY_1" "MY_KEY_2"
```

### Get difference between two sets

```bash
SDIFF "MY_KEY_1" "MY_KEY_2"
```

### Get union of two sets

```bash
SUNION "MY_KEY_1" "MY_KEY_2"
```

### Add element to a sorted set

```bash
ZADD "MY_KEY" "MY_SORT_VALUE" "MY_VALUE"
```

### Get sorted set cardinality

```bash
ZCARD "MY_KEY"
```

### Get subset of sorted set (asc)

```bash
ZRANGE "MY_KEY" SUBSET_START_INDEX SUBSET_END_INDEX (-1 represents the last element) [WITHSCORES]
```

### Get subset of sorted set (desc)

```bash
ZREVRANGE "MY_KEY" SUBSET_START_INDEX SUBSET_END_INDEX (-1 represents the last element) [WITHSCORES]
```

### Get element score on a sorted set

```bash
ZSCORE "MY_KEY" "MY_VALUE"
```

### Get element rank on a sorted set (asc)

```bash
ZRANK "MY_KEY" "MY_VALUE"
```

### Get element rank on a sorted set (desc)

```bash
ZREVRANK "MY_KEY" "MY_VALUE"
```

### Increment integer values on a sorted set

```bash
ZINCRBY "MY_KEY" INCREMENT_VALUE "MY_VALUE"
```

### Decrement integer values on a sorted set

```bash
ZDECRBY "MY_KEY" DECREMENT_VALUE "MY_VALUE"
```
