# 笔试总结

[TOC]

## 数据库

### 关系型数据库和非关系型数据库比较

[关系型数据库和非关系型数据库比较](https://www.jianshu.com/p/fd7b422d5f93)

## others

### 摘要算法、哈希算法

MD5、SHA1, SHA224, SHA256, SHA384, SHA512

它通过一个函数，把任意长度的数据转换为一个==长度固定的数据串==（通常用16进制的字符串表示）。

举个==例子==，你写了一篇文章，内容是一个字符串`'how to use python hashlib - by Michael'`，并附上这篇文章的摘要是`'2d73d4f15c0db7f5ecb321b6a65e5d6d'`。如果有人篡改了你的文章，并发表为`'how to use python hashlib - by Bob'`，你可以一下子指出Bob篡改了你的文章，因为根据`'how to use python hashlib - by Bob'`计算出的摘要不同于原始文章的摘要。

可见，摘要算法就是通过摘要函数`f()`对任意长度的数据`data`计算出固定长度的摘要`digest`，目的是为了发现原始数据是否被人篡改过。

摘要算法之所以能指出数据是否被篡改过，就是因为摘要函数是一个单向函数，==计算`f(data)`很容易，但通过`digest`反推`data`却非常困难==。而且，==对原始数据做一个bit的修改，都会导致计算出的摘要完全不同==。

hashlib模块https://www.liaoxuefeng.com/wiki/897692888725344/923057313018752

**==hash碰撞==**

