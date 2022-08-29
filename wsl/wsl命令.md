# wsl命令

## 格式

### PowerShell或Windows命令提示符

* wsl

### bash/Linux发行版

* wsl.exe

## 基本命令

* 安装特定的linux发行版

```
wsl --install --distribution <Distribution Name>
```

* 列出可用的发行版

```
wsl --list --online
```

* 列出已经安装的发行版

```
wsl --list --verbose
```

* 修改wsl版本为1或2

```
wsl --set-version <distribution name> <versionNumber>
```

* 设置默认版本

```
wsl --set-default-version <Version>
```

```
wsl --set-default <Distribution Name>
```

version 设置为1或2

* 将目录更改为主页

```
wsl ~
```

* 运行特定发行版

```
wsl --distribution <Distribution Name> --user <User Name>
```

## 不常用命令

* 更新wsl

```
wsl --update
```

* 检查wsl状态

```
wsl --status
```

* 获取帮助

```
wsl --help
```

* 以特定用户运行

```
wsl -u <Username>`, `wsl --user <Username>
```

* 更改发行版的默认用户

```
<DistributionName> config --default-user <Username>
```

* 关闭wsl

```
wsl --shutdown
```

* 若要终止指定的发行版或阻止其运行，请将 `<Distribution Name>` 替换为目标发行版的名称。

```
wsl --terminate <Distribution Name>
```

[WSL 的基本命令 | Microsoft Docs](https://docs.microsoft.com/zh-cn/windows/wsl/basic-commands)
