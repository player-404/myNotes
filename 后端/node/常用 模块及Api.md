## - crypto 模块

### 1. 前置知识

#### hex（十六进制）编码:
**十六进制**（_英语：Hexadecimal_，简写为_Hex_或下标16）在是一种逢16进1的进位制。一般用数字0到9和字母A到F表示，其中：A~F相当于十进制的10~15，这些称作**十六进制数字**。

```ad-tip
title: token 是十六进制的
简单token的组成；uid(用户唯一的身份标识)、time(当前时间的时间戳)、sign（签名，token的前几位以哈希算法压缩成的一定长度的**十六进制**字符串。为防止token泄露）。
```

### 2.常用api
#### >randomBytes:
##### 作用：
生成随机子节数
##### api:
```js
crypto.randomBytes( size, callback )
```
#### >createHash
##### 作用：
创建并返回一个哈希对象

##### api:
创建 hash
```js
cosnt hash = createHash('加密算法')
```
加密 值
```js
hash.update(value)
```
返回给定编码的值
```js
const password = has.digest(endcoding)
```

##### 例子：
```js
const crypyo = require("crypto");
// 生成随机的十六进制字符串
const data = crypyo.randomBytes(32).toString("hex");
// 生成hash
const hash = crypyo.createHash("md5");
// 加密
hash.update(data);
// 输出十六进制的加密字符串
const randomToken = hash.digest("hex");
```