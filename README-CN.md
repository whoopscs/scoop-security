<div align="center">
    <h1 align="center">scoop-security</h1>
    <p align="center">
        scoop-security 是一个用于渗透测试和网络安全相关工具下载、安装和自动更新的Scoop软件仓库。
    </p>
    <p align="center">
        <a href="README.md">English</a> | <a href="README-CN.md">简体中文</a>
    </p>
</div>



## 安装

### 安装Scoop

[Scoop安装教程](./Install.md)

### 安装该仓库中的软件

确保你已经有 Scoop 环境，执行以下命令订阅本软件仓库:

```powershell
scoop bucket add sec https://github.com/whoopscs/scoop-security
```

执行以下命令安装本仓库中的软件:

```powershell
scoop install sec/x64dbg
```

## 支持软件

### Apps

| 软件        | 描述         | 安装        |
| ----------- | ----------- | ----------- |
| [afrog](https://github.com/zan8in/afrog) | afrog 是一款性能卓越、快速稳定、PoC 可定制化的漏洞扫描工具</br>A tool for finding vulnerabilities | scoop install afrog |
| [AntSword](https://github.com/AntSwordProject/AntSword-Loader) | AntSword 加载器 | scoop install AntSword |
| [Behinder](https://github.com/rebeyond/Behinder) | “冰蝎”动态二进制加密网站管理客户端 | scoop install Behinder |
| [Godzilla](https://github.com/BeichenDream/Godzilla) | 哥斯拉 | scoop install Godzilla |
| [BlueTeamTools](https://github.com/abc123info/BlueTeamTools) | 蓝队分析研判工具箱，功能包括内存马反编译分析、各种代码格式化、网空资产测绘功能、溯源辅助、解密冰蝎流量、解密哥斯拉流量、解密Shiro/CAS/Log4j2的攻击payload、IP/端口连接分析、各种编码/解码功能、蓝队分析常用网址、java反序列化数据包分析、Java类名搜索、Fofa搜索、Hunter搜索等。 | scoop install BlueTeamTools |
| [BurpSuite](https://portswigger.net) |  | scoop install burpsuite |
| [CobaltStrike](https://www.cobaltstrike.com) |  | scoop install cobaltstrike |
| [commix](https://github.com/commixproject/commix) | 一个开源渗透测试工具，可自动检测和利用命令注入漏洞 | scoop install commix |
| [crawlergo](https://github.com/Qianlitp/crawlergo) | 一款功能强大的浏览器爬虫，用于扫描网页漏洞 | scoop install crawlergo |
| [dddd](https://github.com/SleepingBag945/dddd) | 一款高可拓展的指纹识别、供应链漏洞探测工具。支持从Hunter、Fofa批量拉取目标。 | scoop install dddd |
| [dirmap](https://github.com/H4ckForJob/dirmap) | 一个高级web目录、文件扫描工具，功能将会强于DirBuster、Dirsearch、cansina、御剑 | scoop install dirmap |
| [Dirscan](https://github.com/corunb/Dirscan) | 一款由go编写的高性能、高并发的目录扫描器，现在已经支持GET、HEAD、递归扫描、代理、爬虫等功能功能,后续努力实现更多功能。 | scoop install Dirscan |
| [dirsearch](https://github.com/maurosoria/dirsearch) | web路径扫描 | scoop install dirsearch |
| [dnsx](https://github.com/projectdiscovery/dnsx) | 一个快速和多用途的DNS工具包，用于运行DNS查询 | scoop install dnsx |
| [DudeSuite](https://github.com/x364e3ab6/DudeSuite) | Dude Suite Web 渗透测试工具集 | scoop install DudeSuite |
| [EHole](https://github.com/EdgeSecurityTeam/EHole) | 红队重点攻击系统指纹探测工具 | scoop install EHole |
| [ENScan](https://github.com/wgpsec/ENScan_GO) | 一款基于各大企业信息API的工具，解决在遇到的各种针对国内企业信息收集难题。一键收集控股公司ICP备案、APP、小程序、微信公众号等信息聚合导出。 | scoop install ENScan |
| [ffuf](https://github.com/ffuf/ffuf) | 用 Go 编写的快速 Web 模糊测试器 | scoop install ffuf |
| [fofaviewer](https://github.com/wgpsec/fofa_viewer) | 一个由WgpSec狼组安全团队开发的FoFa客户端数据查看工具，使用JavaFX编写，支持多标签查询、导出Excel文件等功能。 | scoop install fofaviewer |
| [fscan](https://github.com/shadow1ng/fscan) | 一款内网综合扫描工具，方便一键自动化、全方位漏扫扫描。 | scoop install fscan |
| [Fvuln](https://github.com/d3ckx1/Fvuln) | 一款自动化工具，主要适用于日常安全服务、渗透测试人员和RedTeam红队人员，它集合的功能包括：存活IP探测、开放端口探测、web服务探测、web漏洞扫描、smb爆破、ssh爆破、ftp爆破、mssql爆破等其他数据库爆破工作以及大量web漏洞检测模块。 | scoop install Fvuln |
| [GDA](https://github.com/charles2gan/GDA-android-reversing-Tool) | 一个用C++实现的强大的Dalvik字节码反编译器，具有分析速度快，内存磁盘消耗低等优点，对apk、dex、odex、oat、jar、class、aar文件有较强的反编译能力 | scoop install GDA |
| [ghauri](https://github.com/r0oth3x49/ghauri) | An advanced cross-platform tool that automates the process of detecting and exploiting SQL injection security flaws. | scoop install ghauri |
| [goby](https://gobysec.net) | 新一代网络安全技术，通过为目标建立完整的资产数据库，实现快速的安全应急 | scoop install goby |
| [gogo](https://github.com/chainreactors/gogo) | 面向红队的, 高度可控可拓展的自动化引擎 | scoop install gogo |
| [GooFuzz](https://github.com/m3n0sd0n4ld/GooFuzz) | GooFuzz is a tool to perform fuzzing with an OSINT approach. | scoop install GooFuzz |
| [HackBrowserData](https://github.com/moonD4rk/HackBrowserData) | 一款可全平台运行的浏览器数据导出解密工具。 | scoop install HackBrowserData |
| [httpx](https://github.com/projectdiscovery/httpx) | httpx is a fast and multi-purpose HTTP toolkit that allows running multiple probes using the retryablehttp library. It is designed to maintain result reliability with an increased number of threads | scoop install httpx |
| [interactsh](https://github.com/projectdiscovery/interactsh) | An OOB interaction gathering server and client library. | scoop install interactsh |
| [JNDInjector](https://github.com/rebeyond/JNDInjector) | 一个高度可定制化的JNDI和Java反序列化利用工具 | scoop install JNDInjector |
| [JYso](https://github.com/qi4L/JYso) | It can be either a JNDIExploit or a ysoserial. | scoop install JYso |
| [katana](https://github.com/projectdiscovery/katana) | A next-generation crawling and spidering framework. | scoop install katana |
| [kscan](https://github.com/lcvvvv/kscan) | Kscan 是一款纯 go 开发的全方位扫描器，具备端口扫描、协议检测、指纹识别，暴力破解等功能。支持协议 1200+，协议指纹 10000+，应用指纹 2000+，暴力破解协议 10 余种。 | scoop install kscan |
| [ksubdomain](https://github.com/knownsec/ksubdomain) | Subdomain enumeration tool, asynchronous dns packets, use pcap to scan 1600,000 subdomains in 1 second | scoop install ksubdomain |
| [masscan](https://github.com/robertdavidgraham/masscan) | TCP port scanner, spews SYN packets asynchronously, scanning entire Internet in under 5 minutes. | scoop install masscan |
| [MDUT](https://github.com/SafeGroceryStore/MDUT) | MDUT - Multiple Database Utilization Tools | scoop install MDUT |
| [mimikatz](https://github.com/gentilkiwi/mimikatz) | A little tool to play with Windows security | scoop install mimikatz |
| [naabu](https://github.com/projectdiscovery/naabu) | projectdiscovery/naabu: A fast port scanner written in go with a focus on reliability and simplicity. Designed to be used in combination with other tools for attack surface discovery in bug bounties and pentests | scoop install naabu |
| [Neo-reGeorg](https://github.com/L-codes/Neo-reGeorg) | Neo-reGeorg is a project that seeks to aggressively refactor reGeorg. | scoop install Neo-reGeorg |
| [netspy](https://github.com/shmilylty/netspy) | netspy是一款快速探测内网可达网段工具（深信服深蓝实验室天威战队强力驱动） | scoop install netspy |
| [NimScan](https://github.com/elddy/NimScan) | Fast Port Scanner | scoop install NimScan |
| [nuclei](https://github.com/projectdiscovery/nuclei) | Fast and customizable vulnerability scanner based on simple YAML based DSL | scoop install nuclei |
| [observer_ward](https://github.com/emo-crab/observer_ward) | 侦查守卫指纹识别工具 | scoop install observer_ward |
| [OneForAll](https://github.com/shmilylty/OneForAll) | OneForAll是一款功能强大的子域收集工具 | scoop install OneForAll |
| [pagodo](https://github.com/opsdisk/pagodo) | 自动执行 Google Hacking 数据库抓取和搜索 | scoop install pagodo |
| [pocsuite3](https://github.com/knownsec/pocsuite3) | pocsuite3是知道创宇404团队开发的开源远程漏洞测试框架 | scoop install pocsuite3 |
| [quake_rs](https://github.com/360quake/quake_rs) | Quake Command-Line Application | scoop install quake_rs |
| [rad](https://github.com/chaitin/rad) | 一款专为安全扫描而生的浏览器爬虫 | scoop install rad |
| [rustcat](https://github.com/robiot/rustcat) | The modern Port listener and Reverse shell. | scoop install rustcat |
| [RustScan](https://github.com/RustScan/RustScan) | The Modern Port Scanner. | scoop install RustScan |
| [scan4all](https://github.com/GhostTroops/scan4all) | Vulnerabilities Scan；15000+PoC漏洞扫描；[ 23 ] 种应用弱口令爆破；7000+Web指纹；146种协议90000+规则Port扫描；Fuzz、HW打点、BugBounty神器... | scoop install scan4all |
| [sqlmap](https://github.com/sqlmapproject/sqlmap) | sqlmap是一个自动化的SQL注入工具，其主要功能是扫描，发现并利用给定的URL进行SQL注入 | scoop install sqlmap |
| [subfinder](https://github.com/projectdiscovery/subfinder) | Subfinder is a subdomain discovery tool that discovers valid subdomains for websites. Designed as a passive framework to be useful for bug bounties and safe for penetration testing. | scoop install subfinder |
| [suo5](https://github.com/zema1/suo5) | 一款高性能 HTTP 代理隧道工具 | scoop install suo5 |
| [ToolsFx](https://github.com/Leon406/ToolsFx) | 基于kotlin+tornadoFx的跨平台密码学工具箱.包含编解码,编码转换,加解密, 哈希,MAC,签名,大数运算,压缩,二维码功能,ctf等实用功能,支持插件. | scoop install ToolsFx |
| [TscanPlus](https://github.com/TideSec/TscanPlus) | 综合性网络安全检测和运维工具,快速进行资产发现、识别、检测,发现存在的薄弱点和攻击面. | scoop install TscanPlus |
| [Webshell_Generate](https://github.com/cseroad/Webshell_Generate) | 用于生成各类免杀webshell | scoop install Webshell_Generate |
| [woodpecker](https://github.com/woodpecker-framework/woodpecker-framework-release) | 高危漏洞精准检测与深度利用框架 | scoop install woodpecker |
| [xmap](https://github.com/xvvvan/xmap) | xmap 是一个用 JavaFX 编写的用户友好的 FOFA、Hunter 客户端 | scoop install xmap |
| [xpoc](https://github.com/chaitin/xpoc) | xpoc 为供应链漏洞扫描设计的快速应急响应工具 | scoop install xpoc |
| [xray](https://github.com/chaitin/xray) | 一款完善的安全评估工具，支持常见 web 安全问题扫描和自定义 poc | scoop install xray |
| [yakit](https://github.com/yaklang/yakit) | Cyber Security ALL-IN-ONE Platform | scoop install yakit |
| [jar-analyzer](https://github.com/jar-analyzer/jar-analyzer) | 一个JAR包分析工具，批量分析搜索，方法调用关系搜索，字符串搜索，Spring分析，CFG分析，JVM Stack Frame分析，远程分析Tomcat，进阶表达式搜索，自定义SQL查询，字节码查看，命令行分析，使用简易RASP保护 | scoop install jar-analyzer |
| [jar-obfuscator](https://github.com/jar-analyzer/jar-obfuscator) | 一个 JAR/CLASS 字节码混淆工具，支持包名/类名/方法名/字段名/参数名引用分析和重命名混淆方式，支持字符串加密/整型异或混淆/垃圾代码花指令混淆/等方式，支持方法和字段的隐藏，支持 NATIVE 层的 JVMTI 代码加密，配置简单，文档教程齐全，容易上手 | scoop install jar-obfuscator |
| [java-echo-generator](https://github.com/pen4uin/java-echo-generator) | 一款支持高度自定义的 Java 回显载荷生成工具 | scoop install java-echo-generator |
| [java-memshell-generator](https://github.com/pen4uin/java-memshell-generator) | 一款支持高度自定义的 Java 内存马生成工具 | scoop install java-memshell-generator |
| [proguard](https://github.com/Guardsquare/proguard) | ProGuard 是一个免费的 Java 字节码压缩器、优化器、混淆器和预验证器 | scoop install proguard |
| [mitan](https://github.com/kkbo8005/mitan) | 密探渗透测试工具包含资产信息收集，子域名爆破，搜索语法，资产测绘（FOFA，Hunter，quake, ZoomEye），指纹识别，敏感信息采集，文件扫描、密码字典等功能 | scoop install mitan |
| [proxify](https://github.com/projectdiscovery/proxify) | A versatile and portable proxy for capturing, manipulating, and replaying HTTP/HTTPS traffic on the go. | scoop install proxify |
| [xapp](https://github.com/chaitin/xapp) | 专注于web指纹识别的工具 | scoop install xapp |
| [XiebroC2](https://github.com/INotGreen/XiebroC2) | 支持多人协作渗透测试图形框架。</br>Supports multi-person collaborative penetration testing graphical framework. | scoop install XiebroC2 |
| [feroxbuster](https://github.com/epi052/feroxbuster) | 一个用 Rust 编写的快速，简单，递归的内容发现工具。</br>A fast, simple, recursive content discovery tool written in Rust. | scoop install feroxbuster |
| [SharpScan](https://github.com/INotGreen/SharpScan) | C#开发的内网资产扫描器，方便内网横向移动和域内信息收集。 | scoop install SharpScan |
| ...                                                       | ...                                                          | ...                         |



### Burp Suite Extensions

> 增加部分BurpSuite插件自动更新，BurpSuite 添加插件时，请选择插件目录中`current`文件夹下的程序，避免版本更新后需重复添加插件的问题

| 软件        | 描述         | 安装        |
| ----------- | ----------- | ----------- |
| [BurpShiroPassiveScan](https://github.com/pmiaowu/BurpShiroPassiveScan) | 一款基于BurpSuite的被动式shiro检测插件                       | scoop install BurpShiroPassiveScan  |
| [BurpFastJsonScan](https://github.com/pmiaowu/BurpFastJsonScan) | 一款基于BurpSuite的被动式FastJson检测插件                    | scoop install BurpFastJsonScan      |
| [sqlmap4burp-plus-plus](https://github.com/c0ny1/sqlmap4burp-plus-plus) | burp联动sqlmap插件                                           | scoop install sqlmap4burp-plus-plus |
| [HaE](https://github.com/gh0stkey/HaE)                       | Highlighter and Extractor, Empower ethical hacker for efficient operations | scoop install HaE                   |
| [CaA](https://github.com/gh0stkey/CaA)                       | CaA是一个基于BurpSuite Java插件API开发的流量收集和分析插件   | scoop install CaA                   |
| [RouteVulScan](https://github.com/F6JO/RouteVulScan)         | 递归式被动检测脆弱路径的burp插件</br>Route Vulnerable scanning | scoop install RouteVulScan          |
| [TsojanScan](https://github.com/Tsojan/TsojanScan)           | 一个集成的BurpSuite漏洞探测插件</br>An integrated BurpSuite vulnerability detection plug-in. | scoop install TsojanScan            |
| [OneScan](https://github.com/vaycore/OneScan)                | OneScan是递归目录扫描的BurpSuite插件                         | scoop install OneScan               |
| [BypassPro](https://github.com/0x727/BypassPro)              | 对权限绕过自动化bypass的burpsuite插件                        | scoop install BypassPro             |
| [HopLa](https://github.com/synacktiv/HopLa)                  | 一个自动添加，填充测试片段的BurpSuite插件。</br>Adds autocompletion support and useful payloads in Burp Suite. | scoop install HopLa                 |
| ...                                                          | ...                                                          | ...                                 |



### Other Apps

| 软件        | 描述         | 安装        |
| ----------- | ----------- | ----------- |
| [openjdk](https://openjfx.io)                                | 解决部分软件在高版本JAVA运行时缺少javafx依赖的问题           | scoop install openjdk          |
| [notify](https://github.com/projectdiscovery/notify)         | 辅助多个工具的输出并通知到受支持的平台                       | scoop install notify           |
| [npcap](https://npcap.com)                                   | 专为 Windows 开发的一款网络抓包 SDK                          | scoop install npcap            |
| [winscp](https://winscp.net)                                 | 一个Windows环境下使用SSH的开源图形化SFTP客户端               | scoop install winscp           |
| [HashCalculator](https://github.com/hrpzcf/HashCalculator)   | 文件哈希值批量计算器                                         | scoop install HashCalculator   |
| [RevokeMsgPatcher](https://github.com/huiyadanli/RevokeMsgPatcher) | PC版微信/QQ/TIM防撤回补丁                                    | scoop install RevokeMsgPatcher |
| [Everything](https://www.voidtools.com)                      | 文件搜索工具，基于名称快速定位文件和文件夹。</br>Locate files and folders by name instantly. | scoop install Everything       |
| [RustDesk](https://github.com/rustdesk/rustdesk)             | 一个用 Rust 语言编写专为自托管而设计的开源远程桌面软件。</br>An open-source remote desktop application designed for self-hosting. | scoop install RustDesk         |
| [SublimeText](https://www.sublimetext.com/)                  | 一个文本编辑器。</br>A text editor.                          | scoop install SublimeText      |
| [TinyRDM](https://redis.tinycraft.cc/)                       | 一款现代轻量级跨平台 Redis 桌面管理器。</br>A modern lightweight cross-platform Redis Desktop Manager. | scoop install TinyRDM          |
| ...                                                          | ...                                                          | ...                            |



## 疑问
**1. 我想要某个软件，这个仓库里没有！**

开 [issue]，描述你的需求。


**2. 仓库中的某个软件版本落后了，求更新！**

欢迎 Fork 本仓库，修改落后的软件清单，并提交你的拉取请求。



## 致谢
感谢以下仓库在本仓库部分软件规则编写时提供了参考：
- [ScoopInstaller/Scoop: A command-line installer for Windows.](https://github.com/ScoopInstaller/Scoop)
- [chawyehsu/dorado: 🐟 Yet Another bucket for lovely Scoop](https://github.com/chawyehsu/dorado)
- [ScoopInstaller/Extras: 📦 The Extras bucket for Scoop.](https://github.com/ScoopInstaller/Extras)
- [arch3rPro/PST-Bucket](https://github.com/arch3rPro/PST-Bucket)
