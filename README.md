# Scoop

- 集成`fastgit`，能在墙内更快的下载来自`github`的文件
- 为了降低`fastgit`的负担，仅在墙内生效，判断依据能否访问`v2ray.com/robots.txt`
- 增加默认`aria2`下载线程，提高下载速度
- 安装脚本改自`ScoopInstaller/Install`

## 安装

```
[Net.ServicePointManager]::SecurityProtocol=[Net.ServicePointManager]::SecurityProtocol -bor 3072;iwr -useb raw.fastgit.org/star2000/scoop/master/bin/install.ps1 | iex
```

## 用法

```
scoop help
```

## 设置

通过`scoop config <键> <值>`设置

- `键`: 说明
	- `默认值`
	- `可选值1`
	- `可选值2`
> 基本选项
- `proxy`: 代理
	- `none`
	- `default`
	- `currentuser`
	- 代理地址
- `show_update_log`: 显示更新日志
	- `true`
	- `false`
- `aria2-enabled`: 启用aria2
	- `true`
	- `false`
- `aria2-retry-wait`: 重试等待秒数
	- `2`
	- `0`: 不重试
	- 正整数
- `aria2-split`: 单任务连接数
    - `1024`
    - 正整数
- `aria2-max-connection-per-server`: 单服务器最大连接数
    - `16`
    - `1`~`16`
- `aria2-min-split-size`: 最小文件分片大小
    - `1M`
    - `1M`~`1024M`
- `aria2-options`: 其他aria2选项
    - 无
    - ` --键1=值1 --键2=值2`
> 开发者选项
- `debug`: 可被`$env:SCOOP_DEBUG`覆盖
    - `false`
    - `true`
- `rootPath`: 可被`$env:SCOOP`覆盖
    - `$env:USERPROFILE\scoop`
- `globalPath`: 可被`$env:SCOOP_GLOBAL`覆盖
    - `$env:ProgramData\scoop`
- `cachePath`: 可被`$env:SCOOP_CACHE`覆盖
    - `$rootPath\cache`
- `SCOOP_REPO`
	- `https://github.com/star2000/scoop`
- `SCOOP_BRANCH`
    - `master`
- `NO_JUNCTIONS`
    - `false`
    - `true`
- `7ZIPEXTRACT_USE_EXTERNAL`
    - `false`
    - `true`
- `MSIEXTRACT_USE_LESSMSI`
    - `false`
    - `true`
