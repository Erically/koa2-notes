#### 异步的实现方式  
网络访问(api call, database access, etc.)、磁盘读写(disk IO)等都需要异步提升性能
- callback：会有回调黑洞风险
```
const fs = require('fs-extra')
fs.read('file_path', callback)
```

- Promise：
```
const fs = require('fs-extra')
fs.read('file_path').then(fullfill).catch(reject)
```

- async/await
```
const fs = require('fs-extra')
async function readFileTest(){
  await fs.read('file_path')
}
```