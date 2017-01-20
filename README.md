![](https://raw.githubusercontent.com/nripendra/redis-inside/master/icon.png)
#RedisInside-Core

Forked from: https://github.com/poulfoged/redis-inside

Run integration tests in dotnet-core against Redis without having to start/install an instance.

Redis inside works by extracting the Redis executable to a temporary location and executing it. Internally it uses [Redis for windows](https://github.com/MSOpenTech/redis) ported by [MS Open Tech](https://msopentech.com/opentech-projects/redis).


## How to
Launch a Redis instance from just by creating a new instance of Redis. After that the node name and port can be acceessed from the node-property:

```c#
using (var redis = new Redis())
{
    // connect to redis.Endpoint here
}

```

Each instance will run on a random port so you can even run multiple instances:

```c#
using (var redis1 = new Redis())
using (var redis2 = new Redis())
{
    // connect to two nodes here
}

```
## Install

Simply add the Nuget package:

`PM> Install-Package RedisInside-Core`

## Requirements

You'll need .NETCore 1.0 or later on 64 bit Windows to use the precompiled binaries.

## License

Redis Inside is licensed under the two clause BSD license. Redis is copyrighted by Salvatore Sanfilippo and Pieter Noordhuis and released under the [terms of the three clause BSD license](http://redis.io/topics/license).

RedisInside-Core is derivative of Redis Inside and is licensed under the same terms and conditions as Redis Inside.