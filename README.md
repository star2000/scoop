# Scoop

## 改动

-   安装同名包时首选`main`仓库里的
-   添加桶时使用浅克隆加速
-   集成`github镜像`，能在墙内更快的下载来自`github`的文件。为了降低`github镜像`的负担，仅在墙内生效，判断依据能否访问`v2ray.com/robots.txt`
-   调整了`aria2`的默认参数，以最大化下载速度
-   安装脚本改自[`ScoopInstaller/Install`](https://github.com/ScoopInstaller/Install/blob/master/install.ps1)。安装时附带了`apps`桶[`star2000/scoop-apps`](https://github.com/star2000/scoop-apps)，聚合了绝大部分 scoop 桶，开箱即用

## 安装

```powershell
Set-ExecutionPolicy rem -s c;iwr -useb https://ghp.ci/https://raw.githubusercontent.com/star2000/scoop/master/install.ps1 | iex
```

## 用法

```powershell
scoop help
```

## 设置

```powershell
scoop help config
```
