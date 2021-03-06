# 简述对称与非对称加密的概念

### 非对称加密

用公钥加密的数据只能用私钥解密，反过来用私钥加密的数据也只能用公钥解密。

安全性更高，公钥是公开的，密钥是自己保存的，不需要将私钥给别人。缺点：加密和解密花费时间长、速度慢，只适合对少量数据进行加密。

常用的算法：DH、DSA、RSA、ECC。

DH和DSA都不安全，所以现在不常用。

RSA是最常用的，基于**整数分解**的数学难题，密钥长度2048位比较安全。

### 对称加密

用同一个密钥进行加密和解密。

对称加密相比非对称加密算法来说，加解密的效率要高得多、加密速度快。但是缺陷在于对于密钥的管理和分发上比较困难，不是非常安全，密钥管理负担很重。

比如AES、DES、Chacha20。目前DES已经不安全，被废弃。