# vps-shell-mj
整理一些VPS实用脚本，基本一键傻瓜式，对中国小白用户友好

****
## 目录
* [通过yum源命令来安装wget](#通过yum源命令来安装wget)
* [一键测试服务器到国内的速度](#一键测试服务器到国内的速度)
* [一键测试服务器的基本参数](#一键测试服务器的基本参数)
* [测试脚本](#测试脚本)
* [SSR单、多端口一键管理脚本](#一键管理脚本)
* [Shadowsocks 一键安装脚本（四合一）](#一键安装脚本四合一)


### 通过yum源命令来安装wget：
```javascript
yum -y install wget   
```
### 一键测试服务器到国内的速度：

非常的简单，每行一条命令
```javascript
wget https://raw.githubusercontent.com/oooldking/script/master/superspeed.sh
chmod +x superspeed.sh
./superspeed.sh
```
### 一键测试服务器的基本参数：
```javascript
wget -qO- –no-check-certificate https://raw.githubusercontent.com/oooldking/script/master/superbench.sh | bash
```
或者
```javascript
curl -Lso- –no-check-certificate https://raw.githubusercontent.com/oooldking/script/master/superbench.sh | bash
```
### 测试脚本：
```javascript
wget -qO- alicdn.github.io/io.sh | bash
```

## [一键管理脚本](https://www.ubedu.site/archives/528.html)

本脚本适用环境

CentOS 6+, Debian 6+, Ubuntu 14.04 +

安装：
```javascript
wget -N --no-check-certificate https://raw.githubusercontent.com/ToyoDAdoubi/doubi/master/ssr.sh && chmod +x ssr.sh && bash ssr.sh 
```
控制命令：
```javascript
bash ssr.sh    
```

## [一键安装脚本四合一](https://teddysun.com/486.html/comment-page-1)

本脚本适用环境

系统支持：CentOS 6+，Debian 7+，Ubuntu 12+

内存要求：≥128M

使用root用户登录，运行以下命令：
```javascript
wget --no-check-certificate -O shadowsocks-all.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-all.sh
chmod +x shadowsocks-all.sh
./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log
```
若已安装多个版本，则卸载时也需多次运行（每次卸载一种）

使用root用户登录，运行以下命令：
```javascript
./shadowsocks-all.sh uninstall 
```
