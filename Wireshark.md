# Wireshark抓包新手使用教程


Wireshark是非常流行的网络封包分析软件，可以截取各种网络数据包，并显示数据包详细信息。常用于开发测试过程各种问题定位。本文主要内容包括：

    1、Wireshark软件下载和安装以及Wireshark主界面介绍。

    2、WireShark简单抓包示例。通过该例子学会怎么抓包以及如何简单查看分析数据包内容。

    3、Wireshark过滤器使用。过滤器包含两种类型，一种是抓包过滤器，就是抓取前设置过滤规则。另外一种是显示过滤器，就是在数据包分析时进行过滤数据使用。通过过滤器可以筛选出想要分析的内容。包括按照协议过滤、端口和主机名过滤、数据包内容过滤。具体规则和实例可以查看正文。

目录

Wireshark软件安装

Wireshark 开始抓包示例

Wireshakr抓包界面介绍

Wireshark过滤器设置

Wireshark抓包分析TCP三次握手

Wireshark分析常用操作

Wireshark软件安装
软件下载路径：

Wireshark官网下载地址
https://www.wireshark.org/download.html
按照系统版本选择下载，下载完成后，按照软件提示一路Next安装。

说明：如果你是Win10系统，安装完成后，选择抓包但是不显示网卡，下载win10pcap兼容性安装包。下载路径：

win10pcap兼容性安装包


Wireshark 开始抓包示例
先介绍一个使用wireshark工具抓取ping命令操作的示例，让读者可以先上手操作感受一下抓包的具体过程。

1、打开wireshark，主界面如下：![1754839523610](image/Wireshark/1754839523610.png)

2、选择菜单栏上Capture -> Option，勾选WLAN网卡（这里需要根据各自电脑网卡使用情况选择，简单的办法可以看使用的IP对应的网卡）。点击Start。启动抓包。

![1754839649964](image/Wireshark/1754839649964.png)

**3、wireshark启动后，wireshark处于抓包状态中。**

![1754839662899](image/Wireshark/1754839662899.png)

4、执行需要抓包的操作，如在cmd窗口下执行ping www.baidu.com。

5、操作完成后相关数据包就抓取到了。为避免其他无用的数据包影响分析，可以通过在过滤栏设置过滤条件进行数据包列表过滤，获取结果如下。

说明：ip.addr == 119.75.217.26 and icmp 表示只显示ICPM协议且源主机IP或者目的主机IP为119.75.217.26的数据包。协议名称icmp要小写。

![1754839688370](image/Wireshark/1754839688370.png)
**6、wireshark抓包完成，就这么简单。关于wireshark显示过滤条件、抓包过滤条件、以及如何查看数据包中的详细内容在后面介绍。**







————————————————

    版权声明：本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。

原文链接：https://blog.csdn.net/weixin_48916444/article/details/144283540
