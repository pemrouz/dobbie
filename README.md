# Fast, Plain, Distributed Objects 

Open two terminals and run:

```js
const dob = await require('dobbie')('cache-name')
```

In one terminal run: 

```js
dob.foo = 'bar'
```

In the other terminal;

```js
dob
// { foo: 'bar' } 
```

This is a small 5-line Proxy wrapper around [fero](https://github.com/pemrouz/fero). Check out that repo for more information on how it works under the hood (options, replication, partitioning strategies, etc).

Proxies were intentionally not used to avoid any performance issues, however it now seems they may become more optimised hence I thought it would be worth experimenting with. 
