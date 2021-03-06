### 使用多路复用套接字IO提升性能
- Python2.7中的SocketServer模块提供了两个实用类：ForkingMixin和ThreadingMixin.ForxingMixin会为每个客户端请求派生一个新进程
- 或许基于某些原因你不想编写基于进程的应用程序，而更愿意编写多线程应用程序。可能得原因有：
  在线程之间共享应用的状态，避免进程间通信的复杂操作，等等。遇到这种需求，如果想使用SocketServer库编写异步网络服务器，就得使用ThreadingMixIn类

### 文件说明
- chat_server_with_select.py为通过select实现了一个简易的群聊功能
- echo_server_with_diesel.py为使用了Python的diesel包实现异步功能
- forking_mixin_socket_server.py为使用ServerSocket实现一个服务器
- simple_web_server_with_epoll.py为使用epoll实现一个异步通信web服务器
- threading_mixin_socket_server.py使用了多线程实现一个服务器

### select、poll和epoll
