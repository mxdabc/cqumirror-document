---
title: "Homebrew 镜像使用帮助"
draft: false
weight: 2
filepath: '/wiki/mirror-wiki/homebrew/_index'
---

## 地址

https://mirrors.cqu.edu.cn/homebrew/

## 说明

Homebrew 的镜像分为两部分，一个是 formula 索引源，另一个已经打包好的二进制文件的 bottle 源。本镜像为 Homebrew formula 的镜像，对应于 `brew update`，而非 `brew upgrade` 与 `brew install`。


{{% notice note %}}
配置了本源只会提高 `brew update` 的速度，如想提高 `brew upgrade` 和 `brew install` 的速度，请参考[Homebrew-bottles 镜像使用帮助](/wiki/mirror-wiki/homebrew-bottles/_index)配置 bottle 源。
{{% /notice %}}


## 使用说明
### 首次安装
首先，需要确保系统中安装了 bash、git 和 curl，对于 macOS 用户需额外要求安装 Command Line Tools (CLT) for Xcode。
- 对于 macOS 用户，系统自带 bash、git 和 curl，在命令行输入 xcode-select --install 安装 CLT for Xcode 即可。
- 对于 Linux 用户，系统自带 bash，仅需额外安装 git 和 curl。

接着，在终端输入以下几行命令设置环境变量：
```sh
export HOMEBREW_BREW_GIT_REMOTE="https://mirrors.cqu.edu.cn/homebrew/brew.git"
export HOMEBREW_CORE_GIT_REMOTE="https://mirrors.cqu.edu.cn/homebrew/homebrew-core.git"
export HOMEBREW_INSTALL_FROM_API=1
# export HOMEBREW_API_DOMAIN
# export HOMEBREW_BOTTLE_DOMAIN
# export HOMEBREW_PIP_INDEX_URL
```
{{% notice note %}}
建议同时参照[Homebrew-bottles 镜像使用帮助](/wiki/mirror-wiki/homebrew-bottles/)设置`HOMEBREW_API_DOMAIN`和`HOMEBREW_BOTTLE_DOMAIN`，参照[PyPI 镜像使用帮助](/wiki/mirror-wiki/pypi/)设置`HOMEBREW_PIP_INDEX_URL`
{{% /notice %}}
最后，在终端运行以下命令以安装:
```shell
# 从镜像下载安装脚本并安装 Homebrew / Linuxbrew
git clone --depth=1 https://mirrors.cqu.edu.cn/homebrew/install.git brew-install
/bin/bash brew-install/install.sh
rm -rf brew-install

# 也可从 GitHub 获取官方安装脚本安装 Homebrew / Linuxbrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```


### 替换现有仓库上游
 将以下内容添加到 shell 的配置文件中，如 `.zshrc` 或 `.bash_profile` 中，

 ```sh
 export HOMEBREW_BREW_GIT_REMOTE="https://mirrors.cqu.edu.cn/git/homebrew/brew.git"
 export HOMEBREW_CORE_GIT_REMOTE="https://mirrors.cqu.edu.cn/git/homebrew/homebrew-core.git"
 ```

 再 source 对应的 shell 配置文件，运行 `brew update`，即可更新 Homebrew 的 formula 索引。

 更新完成后，运行 `brew config`，检查 `HOMEBREW_BREW_GIT_REMOTE` 和 `HOMEBREW_CORE_GIT_REMOTE` 项，应变为本软件源镜像。

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

