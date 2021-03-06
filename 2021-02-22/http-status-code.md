# 简述常见的 HTTP 状态码的含义



HTTP状态码由三个十进制数组成，第一个数定义了状态码类型，目前，HTTP状态码通常有五个类型：

- 1XX，信息，服务器收到请求，需要请求者继续执行操作
  - 100。继续发送。通知客户端它的部分请求已经被服务器接收，且仍未被拒绝。常见于客户端POST大量数据之前用来探测服务器是否可以接收POST请求。
  - 101。协议升级。服务器已经理解了客户端的请求，并将通过Upgrade 消息头通知客户端采用不同的协议来完成这个请求。常见于websocket协议升级。
- 2XX，成功，操作被成功接收并处理
  - 200。请求成功。最常见的状态码，表示请求已经被服务器正常处理。
- 3XX，重定向，需要进一步操作完成请求
  - 301。永久重定向。请求的站点已经搬家，新的URL在Header中的Location字段中，且可以被搜索引擎收录新URL。
  - 302。临时重定向。跟301类似，不过使用场景有很大不同，使用302重定向通常是临时性重定向或目标URL不固定。
  - 304。未修改。客户端有之前缓存过的文档，发送一个带条件的GET请求，如果缓存内容未改变，则服务器不返回重复内容，客户端将缓存的文档作为请求的响应内容使用。
- 4XX，客户端错误，请求包含语法错误或无法完成请求
  - 401。未授权。客户端缺乏目标资源要求的身份验证凭证。
  - 403。拒绝访问。客户端缺乏访问目标资源的权限。
  - 404。未找到。服务器无法找到目标资源。
  - 405。不允许使用的方法。服务器不支持请求的Method。
  - 499。nginx自己定义的状态码。通常是服务器未返回响应时客户端提前断开连接。
- 5XX，服务器错误，服务器在处理请求的过程中发生了错误
  - 502。网关错误。通常是服务器从上游获取的响应内容异常。
  - 503。服务不可用。通常是服务器在维护中或负载已满。
  - 504。网关超时。通常是服务器从上游获取响应超时。

