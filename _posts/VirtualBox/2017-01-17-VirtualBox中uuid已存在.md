---
layout: post
title:  "VirtualBox中uuid已存在"
date:   2017-01-17 10:14:54
categories: 虚拟化
tags: VirtualBox
---

* content
{:toc}

错误：打开虚拟硬盘失败，UUID already exists

virtualbox在命令行修改虚拟硬盘uuid命令

```

vboxmanage.exe internalcommands sethduuid D:\yourDir\disk.vmdk
```

然后重新就指向disk.vmdk这个虚拟硬盘文件就好了

 
