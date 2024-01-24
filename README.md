
# CTF-NetA: CTF网络流量分析工具
[![Build Status](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](https://download.csdn.net/download/qq_33295410/88301195)
[![GitHub download](https://img.shields.io/github/tag/Arinue/CTF-NetA.svg?label=release)](https://download.csdn.net/download/qq_33295410/88301195)

CTF-NetA是一款专门针对CTF比赛的网络流量分析工具，可以对常见的流量包（.pcapng）进行分析和提取flag，而且还有UI，不需要使用者具备任何基础能力。


![image](https://github.com/Arinue/CTF-NetA/assets/38693947/ba4b74ca-485a-41a1-ad74-415557047771)


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
- 蓝牙流量分析
- 工业控制流量支持MMS
- TLS流量使用keylog_file自动解密分析
- 一键分离文件（导出的部分文件会存在问题，可进行手动导出）
- 一键导出dicom,ftp-data,http,imf,smb,tftp协议对象
- 一键修复错误流量包

## 安装
### <a href="https://download.csdn.net/download/qq_33295410/88301195">点击下载</a>

CTF-NetA无需安装，解压即可使用。

## 使用

你可以使用以下命令来运行CTF-NetA：
`CTF-NetA.exe`

当然更简单的方法是双击打开~~
## 许可

CTF-NetA使用GNU通用公共许可证v3.0进行许可。你可以自由地使用、修改和分发它，只要你遵守许可证的条款和条件。

## 联系

如果你有任何问题、反馈或建议，请随时联系我，当然如果该软件对你有所帮助，希望你能点个Star！
## TODO
### sql盲注
  1. 时间盲注
  2. [*]同样长度的bool盲注

[√] 蓝牙流量

[*] 工业流量
 1. [√] MMS

[√] ssl流量

### other
1. [√]流量包自动修复

## 更新记录
```
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
1.支持扫描端口统计

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
