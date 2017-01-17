---
layout: post
title:  "Docker远程API配置"
date:   2017-01-17 10:14:54
categories: Docker
tags: Docker
---

* content
{:toc}

你要把 docker daemon 绑定到该端口上。默认情况下，docker daemon使用unix socket(unix:///var/run/docker.sock)
先停止docker daemon再重新启动：
service docker stop
docker -d -H unix:///var/run/docker.sock -H 0.0.0.0:4243
之后就可以：
 curl http://127.0.0.1:4243/containers/json


作者：Honglin Feng
链接：https://www.zhihu.com/question/24852884/answer/29215065
来源：知乎
著作权归作者所有，转载请联系作者获得授权。 
