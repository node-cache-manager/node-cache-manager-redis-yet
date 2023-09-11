# Redis store for node cache manager

[![npm version](https://badge.fury.io/js/cache-manager-redis-yet.svg)](https://www.npmjs.com/package/cache-manager-redis-yet) [![codecov](https://codecov.io/gh/node-cache-manager/node-cache-manager-redis-yet/branch/master/graph/badge.svg?token=NX28S97MDF)](https://codecov.io/gh/node-cache-manager/node-cache-manager-redis-yet)

Redis cache store for [node-cache-manager](https://github.com/node-cache-manager/node-cache-manager).

## Installation

```sh
pnpm install cache-manager-redis-yet
```

Or with npm:

```shell
npm install cache-manager-redis-yet
```

## Usage

```ts
const redis = await redisStore({
  socket: {
    host: 'example.com',
    port: 3679,
    tls: true,
  },
  password: 'secret',
  ttl: 86400 * 1000, // a day in milliseconds, can be overridden per cache
});

redis.set('foo', 'bar');
```

## License

Licensed under the [MIT license](./LICENSE).

Fork from [https://github.com/dabroek/node-cache-manager-redis-store](https://github.com/dabroek/node-cache-manager-redis-store)
