
# CTF-NetA: CTF网络流量分析工具
[![Build Status](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](https://download.csdn.net/download/qq_33295410/88301195)
[![GitHub download](https://img.shields.io/github/tag/Arinue/CTF-NetA.svg?label=release)](https://download.csdn.net/download/qq_33295410/88301195)

CTF-NetA是一款专门针对CTF比赛的网络流量分析工具，可以对常见的网络流量进行分析提取flag，软件具有UI，不需要使用者具备任何基础能力。
![image](https://github.com/Arinue/CTF-NetA/assets/38693947/94d79f45-343e-4d8f-b2bd-68ba1abe7cbe)

![image](https://github.com/Arinue/CTF-NetA/assets/38693947/43b96f3d-5c1d-44cd-adef-b6a2cedbb34d)

![image](https://github.com/Arinue/CTF-NetA/assets/38693947/1f1a8540-4b7f-43ca-9c2f-ef7b631ea8ed)

![image](https://github.com/Arinue/CTF-NetA/assets/38693947/b973ed5e-450e-4fbb-889c-96880298a2e7)



## 功能

CTF-NetA具有以下功能：

- 检测明文和常规编码的flag文本
- USB流量还原（包括鼠标和键盘）
- 无线流量暴力破解密码，破解密码后自动分析
- SQL盲注流量分析,支持二分法,支持盲注,自动识别flag
- ICMP流量分析（TTL、DATA.len、DATA、ICMP.code）
- Telnet流量分析
- FTP流量分析(识别登录成功的用户名和密码)
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

## 获取软件
目前程序所有代码都是本人一手敲出来的，花费了大量个人时间，可以加QQ群373967548下载软件，只需捐赠一杯咖啡即可获得永久使用和更新。
CTF-NetA无需安装，解压即可使用。

## 使用

你可以使用以下命令来运行CTF-NetA：`CTF-NetA.exe`，当然更简单的方法是双击打开~~

程序提供傻瓜式一键操作，大部分功能只需要将流量文件拖入程序点击开始分析即可，TLS和CS通信流量分析需要设置对应的TLS.keylog_file路径和.cobaltstrike.beacon_keys路径！

## 许可

CTF-NetA使用<a href="./LICENSE">Apache License 2.0</a>进行许可。你可以自由地使用它，只要你遵守许可证的条款和条件。

## 联系

时间紧工作忙，胡乱堆的代码，如果你发现任何问题，或有其他建议，请加QQ群373967548。当然如果该软件对你有所帮助，希望你能点个Star！
## TODO
- sql盲注
  1. 常规盲注【√】
  2. 单字符查询【√】
  3. ascii数字判断查询【√】
  4. 时间盲注
- Webshell流量分析
1. 菜刀蚁剑常规php流量分析【√】
2. 冰蝎3.x流量解密和分析
3. 冰蝎4.x流量解密和分析
4. 哥斯拉流量解密和分析
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

## 更新记录
```
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
