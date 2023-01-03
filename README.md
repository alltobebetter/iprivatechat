## IprivateChat-ipchat聊天室

> 准备基础：服务器，至少装有node，此README仅为linux服务器部署方式，如果您使用windows服务器，只需要另外开放3000端口命令即可。体验148.100.76.211:3000，可以绑定域名但是懒得绑定了《》

#### 你问我为什么整这个聊天室？

我其实是不愿意整这种聊天室的，本来我的服务器就负载着一个supage云盘还有一个awa论坛以及WordPress，我就想好好的直接安装一个duckchat，结果好像是sqlite还是php版本的原因，说什么也不能安装上，而且官方也放弃了这个项目，我就只能上网搜一搜资料开做了。

#### 开放3000端口

如果没有Firewalls，请先安装，并且使用root

```
#开放3000端口
firewall-cmd --add-port=3000/tcp --permanent
#重载入添加的端口
firewall-cmd --reload
#查询3000端口是否开启成功
firewall-cmd --query-port=3000/tcp
```

#### 安装代码里面的文件

> 如果下载打包压缩包，则跳过这步

下载Github文件（只需要server.js和index.html，css在html里面写入了）

```
npm install --save express
npm install --save socket.io
#以上也可使用cnpm
```

#### node启动

cd进文件夹，然后使用node

```
node server.js
```

完成！够简单吧！
