---
layout: post
title:  "Java中keytool用途"
date:   2017-01-17 10:14:54
categories: Java
tags: Java
---

* content
{:toc}

http://blog.csdn.net/tony1130/article/details/5134318


http://ln-ydc.iteye.com/blog/1335213



keytool -genseckey -alias aestest -keyalg aes -keysize 128 -storetype JCEKS


秘钥库生成
keytool -genkey -alias qfkey -keyalg rsa
秘钥库口令：123456




C:\Users\jishengxu>keytool -genkey -alias qfkey -keyalg rsa -keystore qf.keystor
e
输入密钥库口令:
再次输入新口令:
您的名字与姓氏是什么?
  [Unknown]:  qf.com
您的组织单位名称是什么?
  [Unknown]:  qf
您的组织名称是什么?
  [Unknown]:  qf
您所在的城市或区域名称是什么?
  [Unknown]:  wuhan
您所在的省/市/自治区名称是什么?
  [Unknown]:  hubei
该单位的双字母国家/地区代码是什么?
  [Unknown]:  cn
CN=qf.com, OU=qf, O=qf, L=wuhan, ST=hubei, C=cn是否正确?
  [否]:  是

输入 <qfkey> 的密钥口令
        (如果和密钥库口令相同, 按回车):
 
