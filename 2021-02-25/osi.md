# 简述 OSI 七层模型

## 一、OSI的概念

Open System Interconnect开放系统互连参考模型，是由ISO（国际标准化组织）定义的。它是个灵活的、稳健的和可互操作的模型，并不是协议，是用来了解和设计网络体系结构的。



## 二、OSI模型的目的

规范不同系统的互联标准，使两个不同的系统能够较容易的通信，而不需要改变底层的硬件或软件的逻辑。



## 三、OSI分为哪七层？

OSI把网络按照层次分为七层，由下到上分别为物理层、数据链路层、网络层、传输层、会话层、表示层、应用层。



### **应用层**

> **为应用软件提供接口，使应用程序能够使用网络服务**

常见的应用层协议：

http(80)、https（443）、 dns(53)、ftp(20/21)、smtp(25)、pop3(110)、telnet(23)

### **表示层**

> **数据的解码和编码、加密和解密、压缩和解压缩**

图片：jpg、gif……

音频：mp3、wma、aac……

视频：mp4、avi……

### 会话层

> **负责建立、管理和终止表示层实体之间的会话连接**

在设备或节点之间提供会话控制，协调通信过程,并提供3种不同的方式来组织它们之间的通信，单工、半双工、全双工。

> 单工：BB机，只能收不能发。
> 半双工：对讲机，收的时候不能发，发的时候不能收。
> 全双工：电话，手机，能同时收发。

### **传输层（TCP/UDP）**

> **负责建立端到端的连接，保证报文在端到端之间的传输。**
> **服务点编址、分段与重组、连接控制、流量控制、差错控制。**

### **网络层（IP）**

> **为网络设备提供逻辑地址**
> **进行路由选择、维护路由表，负责将分组数据从源端传输到目的端**

代表：路由器

### **数据链路层（MAC）**

> **在不可靠的物理链路上，提供可靠的数据传输服务，把帧从一跳（结点）移动到另一跳（结点）。**
> **组帧、物理编址、流量控制、差错控制、接入控制**

代表：交换机

### **物理层**

> 负责把逐个的比特从一跳（结点）移动到另一跳（结点）。
> 定义接口和媒体的物理特性（线序、电压、电流）
> 定义比特的表示、数据传输速率、信号的传输模式
> 定义网络物理拓扑（网状、星型、环型、总线型等拓扑）

代表：集线器





## Reference

https://zhuanlan.zhihu.com/p/150766836