---
title: RSA算法
date: 2023-02-03 07:38:06
tags:
- rsa
- 算法积累
categories:
- 技术
---

## RSA算法

### 算法描述

（1）任意选取两个不同的大素数p和q计算乘积

![img](../images/rsa/rsa1.svg)

；

（2）任意选取一个大整数e，满足

![img](../images/rsa/rsa2.svg)

 ，整数e用做加密钥（注意：e的选取是很容易的，例如，所有大于p和q的素数都可用）；

（3）确定的解密钥d，满足

![img](../images/rsa/rsa3.svg)

 ，即

![img](../images/rsa/rsa4.svg)

 是一个任意的整数；所以，若知道e和

![img](../images/rsa/rsa5.svg)

，则很容易计算出d；

（4）公开整数n和e，秘密保存d ；

（5）将明文m（m<n是一个整数）加密成密文c，加密算法为

![img](../images/rsa/rsa6.svg)

（6）将密文c解密为明文m，解密算法为

![img](../images/rsa/rsa7.svg)

然而只根据n和e（注意：不是p和q）要计算出d是不可能的。因此，任何人都可对明文进行加密，但只有授权用户（知道d）才可对密文解密 。
