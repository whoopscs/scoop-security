

## 关于Scoop

Scoop **是一款适用于Windows平台的命令行软件（包）管理工具**。可以通过命令行工具（PowerShell、CMD等）实现软件（包）的安装管理等需求，通过简单的一行代码实现软件的下载、安装、卸载、更新等操作。

**scoop-security** 是用于 Scoop 的软件仓库，本项目旨在提供用于Windows平台渗透测试和网络安全相关工具的快捷安装、管理和自动更新。


## Scoop安装及使用

**安装环境要求：**

- 确保已安装 [Windows PowerShell 5.1](https://aka.ms/wmf5download)或者更高版本[PowerShell](https://aka.ms/powershell)

- 确保以允许`Powershell` 执行本地脚本



### 更改 powershell 脚本执行权限

```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

在windows中默认不允许任何脚本运行，所以我们可以使用 **`Set-ExecutionPolicy`**来改变PowerShell运行环境，共有4种运行权限，如下所示：

- **Restricted**——默认的设置，不允许任何script运行；
- **AllSigned**——只能运行经过数字证书签名的script；
- **RemoteSigned**——运行本地的script不需要数字签名，但是运行从网络上下载的script就必须要有数字签名（使用脚本安装scoop这一等级就行）；
- **Unrestricted**——允许所有的脚本运行；



### 典型安装

在非管理员的PowerShell中运行此命令，以默认配置安装scoop

```powershell
irm get.scoop.sh | iex

#如果你在访问GitHub时遇到网络问题，你可以使用代理，例如：
Invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://gh.llkk.cc/https://raw.githubusercontent.com/scoopinstaller/install/master/install.ps1')
```

> **Scoop** 将默认把所有用户安装的 App 和 **Scoop** 本身置于`C:\Users\<你的用户名>\scoop`



### 高级安装

如果你想高级安装。你可以下载安装程序，然后用参数手动执行它。

```powershell
irm get.scoop.sh -outfile 'install.ps1'

#如果你在访问GitHub时遇到网络问题，你可以使用代理，例如：
curl -o scoop_install.ps1 https://gh.llkk.cc/https://raw.githubusercontent.com/scoopinstaller/install/master/install.ps1
```

> 查看安装程序的所有可配置参数。
>
> ```powershell
> ./scoop_install.ps1 -?
> ```

例如，将 scoop 安装到一个**自定义目录（D:\Scoop）**，并在安装时使用代理

```powershell
./scoop_install.ps1 -ScoopDir 'D:\Scoop' -Proxy 'http://127.0.0.1:7890'
```



### 给scoop设置全局代理

在国内访问github总是不成功，而且scoop的大部分包都在github，那么配置scoop的下载代理，将会极大的提高效率。

```powershell
# 设置全局代理
scoop config proxy 127.0.0.1:7890

# 取消代理：
scoop config proxy None
```



### 安装本软件仓库中的软件

确保你已经有 Scoop 环境后，执行以下命令订阅本软件仓库：


```powershell
//scoop bucket add <仓库别名> <仓库地址>

scoop bucket add sec https://github.com/tldro/scoop-security
```

- 查找软件

```powershell
scoop search sec/nuclei
//或者
scoop search nuclei
```

- 安装本仓库中的软件：

```powershell
scoop install sec/nuclei
//或者
scoop install nuclei
```

大多数情况下，是可以省略仓库别名 `sec/`，只需要执行类似 `scoop install nuclei` 的命令，除非安装的多个仓库都有此软件，则需要指定安装来源仓库

- <span style="color: red;">使用安装的软件</span>
  1. **所有软件均可在任意位置打开命令行，输入文件名直接运行**
  2. 少量EXE可执行文件（Yakit、Goby），将同时在桌面创建快捷方式



### 软件自动更新

本仓库已经添加 github ci 自动化，每隔几个小时会自动更新所有软件到最新版本



### 使用 Scoop

- 查看 scoop 的命令：

```
scoop help
```

- 查看已安装的程序

```
scoop list
```

- 查看哪些程序可以升级

```
scoop status
```

- 更新 scoop

```
scoop update
```

- 更新 app

```
scoop update nuclei
```

- 更新 scoop、bucket、app

```
scoop update *
```

- 卸载软件

```
scoop uninstall nuclei
```

- 一次性卸载多个软件

```
scoop uninstall nuclei httpx
```

**更多详情请官网安装说明书： [ScoopInstaller](https://github.com/ScoopInstaller)**
