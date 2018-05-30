# Sproto Typescript版

#### 项目介绍
Typescript版的sproto，sproto是skynet框架的一个通信模块


#### 安装教程

1. 需要到nodejs的buffer模块，所以首先要安装nodejs，网上有安装教程，这里就不介绍
2. 引用buffer模块，执行　npm install -s @types/buffers

#### 其他情况下
如果是在cocos creator环境下或者其他环境下，没能装上nodejs，那么可以使用buffer目录下的buffer.js模块．  

buffer目录下的文件就是直接拿nodejs　Buffer模块的源码．并在　sproto.ts　的第一行加上
```js
import { Buffer } from "buffer";
```


#### 运行
```js
tsc test.ts
node test.js
```
### 注意
在网络通信过程中，一定要将要发送的 buffer 转成 base64输出，再经网路socket传输，否则对方在接收时会出现乱码．
```js
sendmsg.toString('base64'); // sendmsg的类型是Buffer
```
