---
title: "WSL 镜像使用帮助"
draft: false
weight: 2
filepath: '/wiki/mirror-wiki/github-release/wsl'
---
## 地址

https://mirrors.cqu.edu.cn/github-release/microsoft/WSL/

## 说明
### WSL 简介<sup><a href="https://en.wikipedia.org/wiki/Windows_Subsystem_for_Linux">摘自Wikipedia</a></sup>
适用于Linux的Windows子系统（英语：Windows Subsystem for Linux，简称WSL）是一个为在Windows 10和Windows Server 2019以上能够原生运行Linux二进制可执行文件（ELF格式）的兼容层。

## 收录架构
与上游保持一致
- arm64
- x64
- Universal

## 使用说明

{{% notice note %}}
建议查看官方[帮助文档](https://learn.microsoft.com/zh-cn/windows/wsl/install)中“脱机安装”部分以获取更详细的安装说明。
{{% /notice %}}

1. 访问[主页](/)右侧“获取下载链接”-“常用软件”-“WSL”并选择合适版本下载并安装。
2. 使用管理员权限打开 PowerShell 窗口，并运行 `dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart` 以启用虚拟机平台可选组件。 可能需要重新启动计算机才能生效。
3. 通过 .wsl 文件安装分发版，请访问[WSL Linux 分发版 镜像使用帮助](/wiki/mirror-wiki/wsl-distributions)获取更多信息。
{{% notice note %}}
本站点仅提供部分发行版的 .wsl 文件。
{{% /notice %}}

## 相关链接

官方文档[https://learn.microsoft.com/zh-cn/windows/wsl/install](https://learn.microsoft.com/zh-cn/windows/wsl/install)
