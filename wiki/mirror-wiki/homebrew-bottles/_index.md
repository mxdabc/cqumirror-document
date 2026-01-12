---
title: "Homebrew-bottles 镜像使用帮助"
draft: false
weight: 2
filepath: '/wiki/mirror-wiki/homebrew-bottles/_index'
---

## 地址

https://mirrors.cqu.edu.cn/homebrew-bottles

## 说明
这是 Homebrew 二进制预编译包的镜像。镜像站同时提供 Homebrew 的 formula 索引的镜像（即 brew update 时所更新内容）。请参考 [Homebrew 镜像站使用帮助](wiki/mirror-wiki/homebrew/_index.md)。  

{{% notice note %}}
(Linuxbrew 用户)Linuxbrew 核心仓库（Linuxbrew/brew，版本 >= 3.3.0) 自 2021 年 10 月 25 日被弃用，Linuxbrew 用户应迁移至 homebrew-core。Linuxbrew 用户请依据新的说明进行镜像配置。  
{{% /notice %}}

## 使用说明

{{% notice note %}}
请在运行 brew 前设置环境变量 HOMEBREW_BOTTLE_DOMAIN，值为 https://mirrors.cqu.edu.cn/homebrew-bottles
此外，brew 4.0 及之后的版本使用新的元数据 JSON API 接口，因此还需要设置环境变量 HOMEBREW_API_DOMAIN，值为 https://mirrors.cqu.edu.cn/homebrew-bottles/api
{{% /notice %}}

### 临时替换  

在当前的终端会话中设置环境变量，仅对本次会话有效。

```sh
export HOMEBREW_API_DOMAIN="https://mirrors.cqu.edu.cn/homebrew-bottles/api/"
export HOMEBREW_BOTTLE_DOMAIN="https://mirrors.cqu.edu.cn/homebrew-bottles"
```

### 长期替换
将环境变量添加到 Shell 配置文件中，使其永久生效。

```sh
# 如果使用 Bash
echo 'export HOMEBREW_API_DOMAIN="https://mirrors.cqu.edu.cn/homebrew-bottles/api/"' >> ~/.bash_profile
echo 'export HOMEBREW_BOTTLE_DOMAIN="https://mirrors.cqu.edu.cn/homebrew-bottles"' >> ~/.bash_profile
export HOMEBREW_API_DOMAIN="https://mirrors.cqu.edu.cn/homebrew-bottles/api/"
export HOMEBREW_BOTTLE_DOMAIN="https://mirrors.cqu.edu.cn/homebrew-bottles"
# 如果使用 Zsh
echo 'export HOMEBREW_API_DOMAIN="https://mirrors.cqu.edu.cn/homebrew-bottles/api/"' >> ~/.zprofile 
echo 'export HOMEBREW_BOTTLE_DOMAIN="https://mirrors.cqu.edu.cn/homebrew-bottles"' >> ~/.zprofile
export HOMEBREW_API_DOMAIN="https://mirrors.cqu.edu.cn/homebrew-bottles/api/"
export HOMEBREW_BOTTLE_DOMAIN="https://mirrors.cqu.edu.cn/homebrew-bottles"
```

## 相关链接

{{% notice link %}}
官方主页
https://brew.sh/
{{% /notice %}}


{{% notice link %}}
`brew` 命令文档
https://docs.brew.sh/Manpage
{{% /notice %}}


{{% notice link %}}
文档
https://docs.brew.sh/
{{% /notice %}}


{{% notice link %}}
社区讨论
https://github.com/Homebrew/discussions/discussions
{{% /notice %}}


{{% notice link %}}
Blog
https://brew.sh/blog/
{{% /notice %}}


{{% notice link %}}
软件包
https://formulae.brew.sh/
{{% /notice %}}


{{% notice link %}}
分析数据
https://formulae.brew.sh/analytics/
{{% /notice %}}


{{% notice link %}}
捐助
https://github.com/homebrew/brew#donations
{{% /notice %}}

{{% notice link %}}
Bottles 介绍
https://docs.brew.sh/Bottles.html
{{% /notice %}}