---
redirect_from: /_posts/2023-3-17-Django环境配置与仓库clone/
title: Django环境配置与仓库clone
tags:
  - Django
---

# Django环境配置与仓库clone

```
pip install virtualenv

virtualenv first_env
```

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/微信图片_20230317163556.5f82xylz5fk0.webp)

启动虚拟环境  安装Django

```
cd first_env

cd Scripts

activate

pip insdstall django==2.2.3
```

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/微信图片_202303171635561.2b60ewxfols0.webp)

进入git bash 创建ssh key

```
cd ~

ssh-keygen.exe -t rsa -C ""
```

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/微信图片_202303171635562.53xmekep67o0.webp)

打开公钥 复制粘贴到网站

```
cd .ssh/

cat id_rsa.pub
```

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/微信图片_202303171635563.2m55b8f9ucw0.webp)

进入git lab 输入刚刚复制到的key 并 Add Key

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/微信图片_202303171635565.knbkel0glpc.webp)

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/微信图片_202303171635566.12jyqtdf5ko0.webp)

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/微信图片_202303171635567.2wuxgny08lc0.webp)

选中你要clone的仓库，复制ssh

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/微信图片_202303171635564.4enm8yjaxew0.webp)

进入git bash

在git bash 利用cd 进入你想克隆的文件夹

找到你想要clone的文件位置

```
git clone
```

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/微信图片_202303171635568.4a4go9mfnbi0.webp)

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/批注-2023-03-14-205246.21zv0rkqm95s.webp)