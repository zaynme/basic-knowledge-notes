# 为什么需要序列化？有什么序列化的方式？

## 为什么需要序列化

互联网的产生带来了机器间通讯的需求，而互联通讯的双方需要采用约定的协议，序列化和反序列化属于通讯协议的一部分。现代通讯一般会有跨平台、跨语言的特点，所以就需要序列化来保证通信双方的数据一致性。

## 有什么序列化的方式

- JSON。可读性好，扩展性高，兼容性好，足够简单，应用最为广泛，但性能并不是很出色，空间开销稍大，不适用于某些严格场景，常用于web端
- Protobuf。性能高，解析速度快，但可读性不好，调试比较麻烦，支持的语言也比较少，适用于性能要求很高的RPC
- XML。可读性好，但是性能较差，空间开销很大，只能序列化属性和字段，适用于配置文件



