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
