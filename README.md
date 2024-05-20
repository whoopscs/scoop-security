<div align="center">
    <h1 align="center">scoop-security</h1>
    <p align="center">
        Scoop bucket for Penetration Testing and Cybersecurity related tools.
    </p>
    <p align="center">
        scoop-security 是一个用于渗透测试和网络安全相关工具下载、安装和自动更新的Scoop软件仓库。
    </p>
</div>


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
>

例如，将 scoop 安装到一个**自定义目录（D:\Scoop）**，并在安装时使用代理

```powershell
./scoop_install.ps1 -ScoopDir 'D:\Scoop' -Proxy 'http://127.0.0.1:7890'
```



### 给scoop设置全局代理

在国内访问github总是不成功，而且scoop的大部分包都在github，那么将scoop的下载配置代理，将会极大的提高效率。

```powershell
# 设置全局代理
scoop config proxy 127.0.0.1:7890
```



### 安装该软件仓库中的软件

确保你已经有 Scoop 环境后，执行以下命令订阅本软件仓库：


```powershell
//scoop bucket add <仓库别名> <仓库地址>

scoop bucket add sec https://github.com/s0nd9r/scoop-security
```

- 查找软件

```powershell
scoop search sec/nuclei
//or
scoop search nuclei
```

- 安装本仓库中的软件：

```powershell
scoop install nuclei
```

大多数情况下，是可以省略仓库别名 `sec/`，只需要执行类似 `scoop install nuclei` 的命令，除非安装的多个仓库都有此软件，则需要指定安装仓库来源



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



## Featured Apps

**前往官网实时查看本仓库软件列表：[s0nd9r/scoop-security](https://scoop.sh/#/apps?q=%22https%3A%2F%2Fgithub.com%2Fs0nd9r%2Fscoop-security%22&o=false&n=true&dm=false)**

| Manifest                        | Description                                                  | Site                                                         |
| ------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| afrog                           | afrog 是一款性能卓越、快速稳定、PoC 可定制化的漏洞扫描工具 - A tool for finding vulnerabilities | [GitHub](https://github.com/zan8in/afrog)                    |
| antsword                        | AntSword 加载器                                              | [GitHub](https://github.com/AntSwordProject/AntSword-Loader) |
| behinder                        | “冰蝎”动态二进制加密网站管理客户端                           | [GitHub](https://github.com/rebeyond/Behinder)               |
| blueteamtools                   | 蓝队分析研判工具箱，功能包括内存马反编译分析、各种代码格式化、网空资产测绘功能、溯源辅助、解密冰蝎流量、解密哥斯拉流量、解密Shiro/CAS/Log4j2的攻击payload、IP/端口连接分析、各种编码/解码功能、蓝队分析常用网址、java反序列化数据包分析、Java类名搜索、Fofa搜索、Hunter搜索等。 | [GitHub](https://github.com/abc123info/BlueTeamTools)        |
| dddd                            | 一款高可拓展的指纹识别、供应链漏洞探测工具。支持从Hunter、Fofa批量拉取目标。 | [GitHub](https://github.com/SleepingBag945/dddd)             |
| dnsx                            | dnsx is a fast and multi-purpose DNS toolkit allow to run multiple DNS queries of your choice with a list of user-supplied resolvers. | [GitHub](https://github.com/projectdiscovery/dnsx)           |
| dudesuite                       | Dude Suite Web 渗透测试工具                                  | [GitHub](https://github.com/x364e3ab6/DudeSuite)             |
| ENScan_GO                       | 一款基于各大企业信息API的工具，解决在遇到的各种针对国内企业信息收集难题。一键收集控股公司ICP备案、APP、小程序、微信公众号等信息聚合导出。 | [GitHub](https://github.com/wgpsec/ENScan_GO)                |
| ffuf                            | Fast web fuzzer written in Go                                | [GitHub](https://github.com/ffuf/ffuf)                       |
| fofaviewer                      | 一个由WgpSec狼组安全团队开发的FoFa客户端数据查看工具，使用JavaFX编写，支持多标签查询、导出Excel文件等功能。 | [GitHub](https://github.com/wgpsec/fofa_viewer)              |
| fscan                           | 一款内网综合扫描工具，方便一键自动化、全方位漏扫扫描。       | [GitHub](https://github.com/shadow1ng/fscan)                 |
| fvuln                           | 一款自动化工具，主要适用于日常安全服务、渗透测试人员和RedTeam红队人员，它集合的功能包括：存活IP探测、开放端口探测、web服务探测、web漏洞扫描、smb爆破、ssh爆破、ftp爆破、mssql爆破等其他数据库爆破工作以及大量web漏洞检测模块。 | [GitHub](https://github.com/d3ckx1/Fvuln)                    |
| ghauri                          | An advanced cross-platform tool that automates the process of detecting and exploiting SQL injection security flaws. | [GiitHub](https://github.com/r0oth3x49/ghauri)               |
| goby                            | 新一代网络安全技术，通过为目标建立完整的资产数据库，实现快速的安全应急 | [官网](https://gobysec.net/)                                 |
| godzilla                        | 哥斯拉                                                       | [GitHub](https://github.com/BeichenDream/Godzilla)           |
| gogo                            | 面向红队的, 高度可控可拓展的自动化引擎                       | [GitHub](https://github.com/chainreactors/gogo)              |
| GooFuzz                         | GooFuzz is a tool to perform fuzzing with an OSINT approach. | [GitHub](https://github.com/m3n0sd0n4ld/GooFuzz)             |
| hackbrowserdata                 | 一款可全平台运行的浏览器数据导出解密工具。                   | [GitHub](https://github.com/moonD4rk/HackBrowserData)        |
| httpx                           | httpx is a fast and multi-purpose HTTP toolkit that allows running multiple probes using the retryablehttp library. It is designed to maintain result reliability with an increased number of threads | [GitHub](https://github.com/projectdiscovery/httpx)          |
| interactsh                      | An OOB interaction gathering server and client library.      | [GitHub](https://github.com/projectdiscovery/interactsh)     |
| jar-analyzer                    | 一个JAR包分析工具，批量分析搜索，方法调用关系搜索，字符串搜索，Spring分析，CFG分析，JVM Stack Frame分析，远程分析Tomcat，进阶表达式搜索，自定义SQL查询，字节码查看，命令行分析，使用简易RASP保护 | [GitHub](https://github.com/jar-analyzer/jar-analyzer)       |
| java-echo-generator-release     | 一款支持高度自定义的 Java 回显载荷生成工具                   | [GitHub](https://github.com/pen4uin/java-echo-generator-release) |
| java-memshell-generator-release | 一款支持高度自定义的 Java 内存马生成工具                     | [GitHub](https://github.com/pen4uin/java-memshell-generator-release) |
| jyso                            | It can be either a JNDIExploit or a ysoserial.               | [GitHub](https://github.com/qi4L/JYso)                       |
| katana                          | A next-generation crawling and spidering framework.          | [GitHub](https://github.com/projectdiscovery/katana)         |
| kscan                           | Kscan 是一款纯 go 开发的全方位扫描器，具备端口扫描、协议检测、指纹识别，暴力破解等功能。支持协议 1200+，协议指纹 10000+，应用指纹 2000+，暴力破解协议 10 余种。 | [GitHub](https://github.com/lcvvvv/kscan)                    |
| ksubdomain                      | Subdomain enumeration tool, asynchronous dns packets, use pcap to scan 1600,000 subdomains in 1 second | [GitHub](https://github.com/boy-hack/ksubdomain)             |
| mdut                            | MDUT - Multiple Database Utilization Tools                   | [GitHub](https://github.com/SafeGroceryStore/MDUT)           |
| naabu                           | projectdiscovery/naabu: A fast port scanner written in go with a focus on reliability and simplicity. Designed to be used in combination with other tools for attack surface discovery in bug bounties and pentests | [GitHub](https://github.com/projectdiscovery/naabu)          |
| Neo-reGeorg                     | Neo-reGeorg is a project that seeks to aggressively refactor reGeorg. | [GitHub](https://github.com/L-codes/Neo-reGeorg)             |
| notify                          | Notify is a Go-based assistance package that enables you to stream the output of several tools (or read from a file) and publish it to a variety of supported platforms | [GitHub](https://github.com/projectdiscovery/notify)         |
| nuclei                          | Fast and customizable vulnerability scanner based on simple YAML based DSL | [GitHub](https://github.com/projectdiscovery/nuclei)         |
| observerWard                    | 侦查守卫指纹识别工具                                         | [GitHub](https://0x727.github.io/ObserverWard)               |
| oneforall                       | OneForAll是一款功能强大的子域收集工具                        | [GitHub](https://github.com/shmilylty/OneForAll)             |
| quaker_rs                       | Quake Command-Line Application                               | [GitHub](https://github.com/360quake/quake_rs)               |
| rustcat                         | The modern Port listener and Reverse shell.                  | [GitHub](https://github.com/robiot/rustcat)                  |
| RustScan                        | The Modern Port Scanner.                                     | [GitHub](https://github.com/RustScan/RustScan)               |
| scan4all                        | Vulnerabilities Scan；15000+PoC漏洞扫描；[ 23 ] 种应用弱口令爆破；7000+Web指纹；146种协议90000+规则Port扫描；Fuzz、HW打点、BugBounty神器... | [GitHub](https://github.com/GhostTroops/scan4all)            |
| sqlmap                          | sqlmap是一个自动化的SQL注入工具，其主要功能是扫描，发现并利用给定的URL进行SQL注入 | [GitHub](https://github.com/sqlmapproject/sqlmap)            |
| subfinder                       | Subfinder is a subdomain discovery tool that discovers valid subdomains for websites. Designed as a passive framework to be useful for bug bounties and safe for penetration testing. | [GitHub](https://github.com/projectdiscovery/subfinder)      |
| suo5                            | 一款高性能 HTTP 代理隧道工具                                 | [GitHub](https://github.com/zema1/suo5)                      |
| ToolsFx                         | 基于kotlin+tornadoFx的跨平台密码学工具箱.包含编解码,编码转换,加解密, 哈希,MAC,签名,大数运算,压缩,二维码功能,ctf等实用功能,支持插件. | [GitHub](https://github.com/Leon406/ToolsFx)                 |
| TscanPlus                       | 综合性网络安全检测和运维工具,快速进行资产发现、识别、检测,发现存在的薄弱点和攻击面. | [GitHub](https://github.com/TideSec/TscanPlus)               |
| xmap                            | xmap 是一个用 JavaFX 编写的用户友好的 FOFA、Hunter 客户端    | [GitHub](https://github.com/xvvvan/xmap)                     |
| xpoc                            | xpoc 为供应链漏洞扫描设计的快速应急响应工具                  | [GitHub](https://github.com/chaitin/xpoc)                    |
| xray                            | 一款完善的安全评估工具，支持常见 web 安全问题扫描和自定义 poc | [GitHub](https://github.com/chaitin/xray)                    |
| yakit                           | Cyber Security ALL-IN-ONE Platform                           | [GitHub](https://github.com/yaklang/yakit)                   |
| ...                             | ...                                                          | [GitHub](https://github.com/s0nd9r)                          |



## Question
**1. I want some other apps!**

Please open new app request [issue](https://github.com/s0nd9r/scoop-security/issues) :)

Please consider submitting your new app pull requests to the official buckets if
they satisfy the criteria before opening new app request in my bucket.



## Thanks
- [ScoopInstaller/Scoop: A command-line installer for Windows.](https://github.com/ScoopInstaller/Scoop)
