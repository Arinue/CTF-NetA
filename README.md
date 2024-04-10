
# CTF-NetA: CTF网络流量分析工具
[![Build Status](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](#)
[![GitHub download](https://img.shields.io/github/tag/Arinue/CTF-NetA.svg?label=release)](https://github.com/Arinue/CTF-NetA/releases)
<a href="https://qm.qq.com/q/FPn1EK1cYO>373967548"><img src="https://img.shields.io/badge/QQ%E7%BE%A4-373967548-orange?style=flat-square" alt="QQGroup"></a>
CTF-NetA是一款专门针对CTF比赛的网络流量分析工具，可以对常见的网络流量进行分析提取flag，软件具有UI，不需要使用者具备任何基础能力。
## 获取软件
编写该程序花费了本人大量时间，只需捐赠一杯咖啡即可获取并永久使用该软件（捐赠后加群联系群主）,另外<a href="https://qm.qq.com/q/FPn1EK1cYO>373967548">点击链接加入群聊【CTF流量分析讨论】不定时赠送注册码</a>，后期将持续更新更多功能。

---
![image](https://github.com/Arinue/CTF-NetA/assets/38693947/5193b59d-fd74-40ea-b2fa-974f47e51041)



## 功能

CTF-NetA具有以下功能：

- 检测明文和常规编码的flag文本
- USB流量还原（包括鼠标和键盘）
- 无线流量暴力破解密码，破解密码后自动分析
- SQL盲注流量分析,支持二分法,支持盲注,自动识别flag
- ICMP流量分析（TTL、DATA.len、DATA、ICMP.code）
- Telnet流量分析
- FTP/FTP-DATA流量分析
- SMTP流量分析(识别登录成功的用户名和密码)
- cs通信流量解密分析（需要提供.cobaltstrike.beacon_keys）
- 蓝牙流量分析
- 工业控制流量支持MMS、modbus、iec60870,mqtt,s7com,OMRON
- TLS流量使用keylog_file自动解密分析
- 一键分离文件（导出的部分文件会存在问题，可进行手动导出）
- 一键导出dicom,ftp-data,http,imf,smb,tftp协议对象
- 一键修复错误流量包
- 识别端口扫描（开放的端口）
- DNS流量分析
- 自动保存HTTP传输文件
- webshell流量一键自动识别和解密

## 使用

CTF-NetA无需安装，解压即可使用。你可以使用以下命令来运行CTF-NetA：`CTF-NetA.exe`，当然更简单的方法是双击打开~~

程序提供傻瓜式一键操作，大部分功能只需要将流量文件拖入程序点击开始分析即可，TLS和CS通信流量分析需要设置对应的TLS.keylog_file路径和.cobaltstrike.beacon_keys路径！

## 许可

CTF-NetA使用<a href="./LICENSE">MT @ M1r4n</a>进行许可。你可以自由地使用它，只要你遵守许可证的条款和条件。

## 联系

时间紧工作忙，胡乱堆的代码，如果你发现任何问题，或有其他建议，请加QQ群373967548反馈。当然如果该软件对你有所帮助，希望你能点个Star！
## 圈钱
![支付宝](https://github.com/Arinue/CTF-NetA/assets/38693947/e24b4665-a636-4c03-9b1d-d6a2db3d79cd)
![image](https://github.com/Arinue/CTF-NetA/assets/38693947/74438f6f-8e2e-4fd2-aa99-f2f34188ca79)

## TODO
- sql盲注
  1. 常规盲注【√】
  2. 单字符查询【√】
  3. ascii数字判断查询【√】
  4. 时间盲注
- Webshell流量分析
1. 菜刀蚁剑常规php流量分析【√】
2. 冰蝎3.x流量解密和分析【√】
3. 冰蝎4.x流量解密和分析【√】
4. 哥斯拉流量解密和分析【√】
- 工控流量
1. Modbus 【√】
2. MMS【√】
3. IEC60870【√】
4. MQTT【√】
5. CoAP
6. COTP
7. IEC104
8. IEC61850
9. S7comm【√】
10. OMRON【√】
- 综合分析
  1.  cobaltstrike 流量解密 【√】
  2.  蓝牙流量分析【√】
  3.  USB流量分析【√】
  4.  shiro流量解密和分析
  5.  struts2流量解密和分析
  6.  哥斯拉wenshell识别和解密【*】
 哥斯拉4.0 php【√】
 哥斯拉4.0 jsp【√】
 哥斯拉4.0 asp

  8.  冰蝎wenshell识别和解密
     冰蝎4.1 php【√】
     冰蝎4.1 jsp【√】
  10.  蚁剑webshell识别和解密【√】
  11.  菜刀webshell识别和解密【√】
- 协议
  1. DNS 【√】
  2. FTP 【√】
  3. SMTP 【√】
  4. TLS 【√】
  5. TELNET 【√】
  6. MYSQL 【√】
  7. REDIS 【√】
  8. ICMP 【√】
  9. 
- other
  1. 更新可选分析协议和内容【√】
  2. 优化UI和运行速度 【√】
  3. 可添加自定义工具
  4. USB鼠标流量优化
  5. 


## 更新记录
```
v1.2.1 20240409
1.支持ETL类型流量转PCAPNG
2.改关键字匹配时全文输出为精简输出（关键字前30至后80）
3.添加检测到http关键的包序号

v1.2.0 20240408
1.支持输出控制台多个关键字遍历查找并高亮
2.修复多处已知BUG
3.部分UI调整

v1.1.6 20240407
1.支持中间件日志SQL注入查询单个字符识别(例题：Example\SQL盲注日志\字符型注入.log)
2.增加wifi流量分析和破解密码兼容性
3.支持UDP协议DATA数据识别

v1.1.5 20230402
1.修复sql日志分析闪退BUG
2.支持ICMP协议frame.len长度识别
3.添加全局flag关键字高亮

v1.1.4 20240326
1.添加更新检查
2.优化优先检查流量中传输的webshell密钥
3.支持自定义工具和插件
4.修复多处BUG

v1.1.3 20240326
1.调整Behinder4_PHP_WITH_AES解密中增加16位冗余数据处理
2.菜刀蚁剑webshell流量解密功能重构上线

v1.1.2 20240324
1.修复存在自定义关键是错误正则时闪退
2.支持优先检查流量中传输的webshell密钥，再进行暴力破解
3.修复哥斯拉流量解密中因数据异常导致的跳过解密

v1.1.1 20240322
1.添加手动控制程序停止功能（防止卡死和全功能分析时间过长的情况）

v1.1.0 20240321
1.哥斯拉和冰蝎支持自定义密钥解密（自动识别加密类型）
2.支持冰蝎3的php和jsp自动识别和暴力破解密钥解密
3.优化暴力破解字典设置为全局使用和可保存到配置文件下

v1.0.3 20240319
1.webshell解密后高亮关键字"flag"
2.修复ftp协议中分段传输文件自动保存不完整的问题
3.支持冰蝎4.1 php和java各种加密类型的webshell识别及解密，自动暴力破解密钥。
4.修复部分关键高亮异常BUG

v1.0.2 20240311
1.优化telnet流量分析，按照IP整理消息，处理特殊按键输入
2.更换4.2.0版本的tshark
3.支持哥斯拉4webshell php（PHP_XOR_BASE64、PHP_XOR_RAW、PHP_EVAL_XOR_BASE64）和jsp（JAVA_AES_BASE64、JAVA_AES_RAW）识别及解密，自动暴力破解密钥。

v1.0.1 20240308
1.更改UI使用pyqt6编写
2.支持哥斯拉4.0（PHP_EVAL_XOR_BASE64）流量识别和解密

v0.4.4 20240304
1.支持SQL注入中间件日志分析

v0.4.3 20240301
1.修复FTP不同版本流量区别，添加操作命令展示
2.支持FTP-DATA传输文件自动保存
3.更改HTTP文件下载保存到output文件夹下
4.修复诸多BUG
5.优化手动修改sql注入正则输入体验

v0.4.2 20240229
1.修复HTTP文件下载识别中media.type数据同步出错闪退
2.更改关键字识别为可选、功能管理滑动条
3.支持TCP DATA数据检测和识别，例题在"\Example\TCPDATA\zip.pcapng"

v0.4.1 20240228
1.优化启动速度，加快4s左右。
2.修复CS流量分析中数据解析异常闪退BUG
3.修复sql盲注中数据未对齐闪退BUG

v0.4.0 20240226
1.支持ICMP IDBE和IDLE识别，添加识别结果关键字高亮
2.修复多处已知BUG

v0.3.9 20240226
1.修复多处闪退BUG
2.支持http post请求的sql盲注

v0.3.8 20240225
1.支持IPID数据提取
2.添加webshell流量解密信息关键字高亮
3.支持自动保存HTTP传输（包括分段传输）的文件

v0.3.7 20240224
1.优化modbus协议分析，添加word_cnt数据提取
2.优化USB键盘流量分析，处理特殊按键

v0.3.6 20240223
1.使用AI识别SQL盲注语句，SQL盲注识别率大大增加

v0.3.5 20240223
1.支持自定义暴力破解字典
2.添加自动分析功能管理
3.修复多处BUG

v0.3.4 20240223
1.支持识别菜刀蚁剑webshell（php）流量和自动解码
2.修复多处BUG

v0.3.3 20240222
1.支持分析DNS协议

v0.3.2 20240221
1.支持分析工控协议mqtt
2.支持分析工控协议s7comm
3.支持分析工控协议omron

v0.3.1 20240221
1.支持分析工控协议modbus
2.支持分析工控协议iec60870

v0.3.0 20240220
1.支持cs流量解密分析（需要提供.cobaltstrike.beacon_keys）
2.修复MMS流量分析BUG。

v0.2.9 20240130
1.加入其他工具（CyberChef）

v0.2.8 20240123
1.优化蓝牙流量分析
2.优化ICMP协议分析
3.优化SQL盲注判断条件
4.添加日志自动清理选项

v0.2.7 20230119
1.支持一键修复流量包
2.支持SMTP协议登录分析
3.修复多处BUG

v0.2.6 20240118
1.支持TLS流量解密，需设置tls.keylog_file
2.支持工业控制协议MMS分析

v0.2.5 20240116
1.支持sql正则可选自动识别
2.分析蓝牙协议，探测pin码，识别传输文件信息

v0.2.4 20240111
1.优化鼠标流量画图机制
2.部分UI设计调整

v0.2.3 20240110
1.支持扫描端口统计（开放的端口）

v0.2.2 20240109
1.支持一键导出文件功能，支持协议：dicom,ftp-data,http,imf,smb,tftp
2.FTP登录包分析，识别登录成功的用户名和密码
3.优化多处BUG

v0.2.1 20240108
1.支持一键分离（foremost）文件，支持任何文件
2.支持SQL注入正则自动识别

v0.2.0 20240107
1.修改ui为自适应分辨率和自适应窗口大小
2.更新UI
3.支持telnet流量分析

v0.1.35
1.支持ICMP流量分析

v0.1.34 
1.支持配置保存和导入按钮

v0.1.33
1.修复部分bug。
2.修复wifi流量破解密码后重新分析数据异常。
```

## 感谢

感谢以下项目：

> https://github.com/gchq/CyberChef
> 
> https://github.com/5ime/CS_Decrypt
>
> https://gitee.com/fengerxi/large-set-of-ctf-flow-problems
