---
redirect_from: /_posts/2023-3-17Django环境配置与仓库clone/
title: Django环境配置与仓库clone
tags:
  - Django
---

# Django环境配置与仓库clone

```
pip install virtualenv

virtualenv first_env
```

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/批注-2023-03-14-202519.5fuj4w511cg0.webp)

```
cd first_env

cd Scripts

activate
```

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/批注-2023-03-14-203359.44r9yq1iqzq0.webp)

进入git bash

```
cd ~

ssh-keygen.exe -t rsa -C ""
```

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/批注-2023-03-14-204107.2i1ncfezqwu0.webp)

```
cd .ssh/

cat id_rsa.pub
```

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/批注-2023-03-14-204311.2pvqx7pupoo0.webp)

进入git lab 输入key 并 Add Key

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/批注-2023-03-14-204752.72pvcj356as0.webp)

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/批注-2023-03-14-204810.6tvc8a91frg0.webp)

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/批注-2023-03-14-204845.1xc9xni80txc.webp)

选中你要clone的仓库，复制ssh

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/批注-2023-03-14-204606.331nl0h73y00.webp)

进入git bash

找到你想要clone的文件位置

```
git clone
```

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/批注-2023-03-14-205100.3m9yeckkqp60.webp)

![](https://cdn.staticaly.com/gh/ElaborateBury/Net-Imagine@master/Imagine/批注-2023-03-14-205246.5qyhq2j01z00.webp)