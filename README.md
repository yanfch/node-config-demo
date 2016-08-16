## node-config demo

### Example

```
node app

var config = require('config'); // => 'development'

console.log(config.get('Wechat.redis')) // =>  { host: '192.168.40.52', port: 6379, db: 0 }

```

```
NODE_ENV=test node app

var config = require('config'); // => 'test'

console.log(config.get('Wechat.redis')) // =>  { host: '172.17.20.107', port: 39000, db: 0 }

```

```
NODE_ENV=production node app

var config = require('config'); // => 'production'

console.log(config.get('Wechat.redis')) // =>  { host: '172.17.20.88', port: 39000, db: 0 }
```