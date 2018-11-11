---
title: Windows下操作POP3
copyright: true
date: 2018-11-10 12:11:12
tags: [pop3, telnet]
categories: 计算机网络
top: 15
---

## Windows10下开启telnet服务    
在自学*《计算机网络-自顶向下方法》*这本书中，`telnet`这个服务命令出现了好多次，  <!-- more -->
开始在*Ubuntu 12.0*终端下输入`telnet`是有正确响应的，但是在*windows 10*命令行下    
输入提示找不到该命令，直到今天我才发现该服务在*window 1o*下是默认关闭的，需要手动打开      
开启步骤如下    
### 1.用小娜以关键词*功能*找到*开启和关闭Windows功能*     
![](https://i.imgur.com/uDffqOV.png)      
其实不一定要这样操作，找到*开启和关闭Windows功能*即可      
### 2.勾选*Telnet客户端*并确定    
![](https://i.imgur.com/ZpsU915.png)    
然后就可以愉快地在windows10玩耍telnet了     

## Windows下操作POP3    
pop3是一个邮件访问协议   
### 1.在cmd下输入`telnet pop3.163.com 110`登录到qq的POP3服务器的110端口      
### 2.依次输入`user csu_xiaotao`和`pass xxxxxxxxx`登录到自己的邮箱   
需要注意的是,`xxxxxxxxx`是邮箱的授权码，不是登录密码    
### 3.然后是一些常见的pop3命令(大小写敏感）    
#### 1.`list`列出所有的收到的邮件，特别的`list n'列出第n封邮件    
其响应格式如下:    
`n m`
其中n为第n封邮件，m为第n封邮件的字节大小    
#### 2.`retr n`下载第n封邮件    
其响应格式如下：       
![](https://i.imgur.com/lQJLbpd.png)    
采用了特殊的编码格式，我们可能看不懂     
#### 3.`dele n`删除第n封邮件    
#### 4.`uidl n`返回第n封邮件的唯一标识   
#### 5.`quit`退出
注意`+OK`代表操作成功；`-ERR`代表操作失败     
