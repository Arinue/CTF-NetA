# CTF-NetA: CTF网络流量分析工具

CTF-NetA是一款专门针对CTF比赛的网络流量分析工具，可以对常见的流量包（.pcapng）进行分析和提取flag，而且还有UI，不需要使用者具备任何基础能力。
![image](https://github.com/Arinue/CTF-NetA/assets/38693947/0ecc7d40-d3c7-4e37-abe6-67f99397de1d)

## 功能

CTF-NetA具有以下功能：

- 检测明文和常规编码的flag文本
- USB流量还原（包括鼠标和键盘）
- 无线流量暴力破解密码，破解密码后自动分析
- SQL盲注流量分析,支持二分法
- ICMP流量分析（TTL、DATA.len、DATA、ICMP.code）
- Telnet流量分析
- FTP流量分析(识别登录成功的用户名和密码)
- 蓝牙流量分析
- 一键分离文件（导出的部分文件会存在问题，可进行手动导出）
- 一键导出dicom,ftp-data,http,imf,smb,tftp协议对象

## 安装

CTF-NetA无需安装，解压即可使用。

## 使用

你可以使用以下命令来运行CTF-NetA：
`CTF-NetA.exe`

当然更简单的方法是双击打开~~
## 许可

CTF-NetA使用GNU通用公共许可证v3.0进行许可。你可以自由地使用、修改和分发它，只要你遵守许可证的条款和条件。

## 联系

如果你有任何问题、反馈或建议，请随时联系我，当然如果你愿意，我希望你能点一个Star
## TODO
sql盲注
1. 时间盲注
2. 同样长度的bool盲注

蓝牙流量

工业流量

ssl流量

other
1. 流量包自动修复
