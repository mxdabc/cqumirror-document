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

## 镜像替换方法

### 临时替换  

在当前的终端会话中设置环境变量，仅对本次会话有效。

```sh
export HOMEBREW_API_DOMAIN="https://mirrors.cqu.edu.cn/homebrew-bottles/api/"
export HOMEBREW_BOTTLE_DOMAIN="https://mirrors.cqu.edu.cn/homebrew-bottles"
```

### 长期替换
将环境变量添加到您的 Shell 配置文件中，使其永久生效。  
- 如果你使用 Bash:将以下内容添加到 ~/.bash_profile 文件中：

```sh
echo 'export HOMEBREW_API_DOMAIN="https://mirrors.cqu.edu.cn/homebrew-bottles/api/"' >> ~/.bash_profile
echo 'export HOMEBREW_BOTTLE_DOMAIN="https://mirrors.cqu.edu.cn/homebrew-bottles"' >> ~/.bash_profile
export HOMEBREW_API_DOMAIN="https://mirrors.cqu.edu.cn/homebrew-bottles/api/"
export HOMEBREW_BOTTLE_DOMAIN="https://mirrors.cqu.edu.cn/homebrew-bottles"
 ```

- 如果你使用 Zsh:将以下内容添加到 ~/.zprofile 文件中：

```sh
echo 'export HOMEBREW_API_DOMAIN="https://mirrors.cqu.edu.cn/homebrew-bottles/api/"' >> ~/.zprofile 
echo 'export HOMEBREW_BOTTLE_DOMAIN="https://mirrors.cqu.edu.cn/homebrew-bottles"' >> ~/.zprofile
export HOMEBREW_API_DOMAIN="https://mirrors.cqu.edu.cn/homebrew-bottles/api/"
export HOMEBREW_BOTTLE_DOMAIN="https://mirrors.cqu.edu.cn/homebrew-bottles"
```

⚠️ 注意 (Linuxbrew 用户)Linuxbrew 核心仓库（Linuxbrew/brew，版本 >= 3.3.0) 于 2021 年 10 月 25 日被弃用，Linuxbrew 用户应迁移至 homebrew-core。Linuxbrew 用户请依据新的说明进行镜像配置。

