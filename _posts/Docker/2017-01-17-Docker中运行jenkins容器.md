---
layout: post
title:  "Docker中运行jenkins容器"
date:   2017-01-17 10:14:54
categories: Docker
tags: Docker
---

* content
{:toc}

docker运行jenkins容器

```


docker run -d -p 8080:8080 -p 50000:50000 --name jenkins-test -v /var/jenkins_home/:/var/jenkins_home jenkins:2.7.3

```



错误信息：

```


touch: cannot touch ‘/var/jenkins_home/copy_reference_file.log’: Permission denied
Can not write to /var/jenkins_home/copy_reference_file.log. Wrong volume permissions?
```



解决办法：挂载的目录/var/jenkins_home/在jenkins容器中没有权限，容器中的jenkins uid是1000，我们对给目录所有者设置为1000即可

```


chown -R 1000 data
```



docker获取容器id

```

docker inspect --format='{{.NetworkSettings.IPAddress}}' $CONTAINER_ID

``` 
