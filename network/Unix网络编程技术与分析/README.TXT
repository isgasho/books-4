                                 程序文件说明

prg1_1.c  :  简单的网络编程实例。该实例是一个客户端程序，它首先连接到一个标准时
间服务器上，从服务器读取当前时间，然后显示时间。

prg4_1.c  :  TCP服务器。该程序等待客户的连接，一旦连接，则显示客户IP地址，并
发信息回客户。

prg4_2.c  :  TCP客户机。该程序完成了TCP套接字客户端的基本过程。

prg5_1.c  :  UDP服务器。该程序执行UDP套接字服务端的基本过程。

prg5_2.c  :  UDP客户。该程序通过命令行参数输入服务器IP地址和发给服务器的信息，然
后执行UDP套接字客户端的基本过程。

prg6_1.c  :  重复性服务器。该程序等候客户连接，一旦连接则显示客户的地址，然后接
收来自该客户的信息（字符串）。每当收到一个字符串，则显示该字符串，并将字符串反转，
再将反转的字符发回客户。之后，继续等待接收该客户的信息直至该客户关闭连接。完成与
该客户交互后，服务器开始等待下一客户，并重复上述过程。

prg6_2.c  :  客户端程序。该程序首先与相应服务器连接。然后接收用户从标准输入（键
盘）输入的字符串，再将字符串发送给服务器，接收服务器发回的信息并显示。之后，继续
等待用户输入直至用户输入Ctrl-D。当收到用户输入Ctrl-D后，客户关闭连接并退出。

prg6_3.c  :  多进程并发服务器。该程序等候客户连接，一旦连接则显示客户的地址，接着
接收该客户的名字并显示。然后接收来自该客户的信息（字符串）。每当收到一个字符串，
则显示该字符串，并将字符串反转，再将反转的字符发回客户。之后，继续等待接收该客户
的信息直至该客户关闭连接。服务器具有同时处理多客户的能力。

prg6_4.c  :  客户程序。该程序首先与相应服务器连接。接着接收用户从标准输入（键盘）
输入的客户名字，再将名字发送给服务器。然后接收用户从标准输入（键盘）输入的字符串，
再将字符串发送给服务器，接收服务器发回的信息并显示。之后，继续等待用户输入直至用
户输入Ctrl-D。当收到用户输入Ctrl-D后，客户关闭连接并退出。

prg6_5.c  :  多线程并发服务器。该程序实现多线程并发服务器。

prg6_6.c  :  线程安全实例。该程序说明线程安全问题。该例子实现的功能与多线程并发
服务器实例的类似，但增加了一个客户数据存储功能，即服务器将存储每个连接客户所发
来的所有数据，当连接终止后，服务将显示客户的名字及相应的数据。

prg6_7.c  :  TSD线程安全实例。该程序采用TSD方法解决线程安全问题。

prg6_8.c  :  通过使用函数的参变量实现线程安全的实例。

prg6_9.c  :  单线程并发服务器实例。该程序采用单线程并发服务器算法实现的。

prg7_1.c  :　主机名转换为IP地址程序。该程序通过用户输入的主机名获得主机实体，然
后显示主机的正式名字、别名和IP地址。

prg7_2.c  ： IP地址转换为主机名程序。该程序通过用户输入的字符串形式的IP地址获
得主机实体，然后显示主机的正式名字、别名和IP地址。

prg8_1.c  ： 互斥对象实例。该程序说明如何使用互斥对象。

prg8_2.c  ： 条件变量实例。该程序是一个多线程的无连接并发服务器。

prg8_3.c  :  处理同步线程退出。

prg8_4.c  :  服务器死锁实例。该程序说明死锁是如何产生的。

prg8_5.c  ： 僵死进程处理程序。该程序捕获SIGCHLD信号，然后调用waitid函数处理僵死进程。

prg8_6.c  ： FIFO服务器实例。其产生一个管道，用于接收客户发来的信息。将收到的字符串
转换为大写字母，再通过客户创建的管道发回到相应的客户。

prg8_7.c  ： FIFO客户实例。客户程序首先打开服务器管道，然后创建自己的管道，通过服务器
管道发送信息给服务器，并且通过自己创建的管道接收服务器发回的信息。

prg9_1.c  ： 服务器异常处理实例。该程序对socket()调用异常采用终止程序的方法处
理。对于accept()和send()调用异常而言，如果是EINTR错误则重新调用该函数，否则终止
程序；对于recv()的调用异常，如果是EINTR错误则重新调用该函数，如果是超时错误则终
止连接，显示超时信息并结束该进程。

[prg10_1]  ： 聊天室实例。其分为服务器和客户两部分。客户首先与服务器建立TCP连
接，并发送客户名称给服务器，然后就可以通过服务器发信息给其他已连接的客户，同时通
过服务器接收其他客户的信息。

prg11_1.c  ： 守护进程实例。该程序实现以守护进程方式运行的聊天室服务
器。       

prg12_1.c  ： 原始套接字实例。其实现一个简单的ping程序。

prg13_1.c  ： 数据链路访问实例。该程序实现捕获所需的包并显示。  

prg14_1.c  ： 单个服务器绑定到多个接口实例。该程序绑定于所有IP地址上且端口号
为1234，当与客户建立连接后显示被连接的IP地址及端口号。 

prg14_2.c  ： 多个服务器绑定到多个接口实例。该程序通过命令行参数获得该服务器所
绑定的地址，服务器完成地址绑定后侦听客户连接并服务客户。  

prg15_1.c  ： 路由套接字实例。该程序从命令行参数读入目的地址，创建路由套接字，
发送RTM-GET消息给系统核，然后通过路由套接字读取返回的路由信息并显示。

[prg16_1]  ： 简单路由器实例。该程序是一个专用的IP路由器，完成IP包的路由功能，
并且通过专用的传输设备/网络传输IP包，使得两个基于TCP/IP的网络可以通过专用传输
设备/网络进行互连。

  
