# vps-shell-mj
整理一些VPS实用脚本，基本一键傻瓜式，对中国小白用户友好

****
## 目录
* [GCP、AWS延迟测试工具](#延迟测试工具)
* [通过yum源命令来安装wget](#通过yum源命令来安装wget)
* [一键测试服务器到国内的速度](#一键测试服务器到国内的速度)
* [一键测试服务器的基本参数](#一键测试服务器的基本参数)
* [测试脚本](#测试脚本)
* [SSR单、多端口一键管理脚本](#一键管理脚本)
* [Shadowsocks 一键安装脚本（四合一）](#一键安装脚本四合一)
* [Centos/Ubuntu/Debian BBR加速一键安装包](#加速一键安装包)
* [CentOS更换内核，提供锐速可用的内核下载](#提供锐速可用的内核下载)






### 延迟测试工具：
今天看到2个工具，可能对各位选择适合自己的GCP（Google Cloud Platform，服务器名称：GCE）、AWS（Amazon Web Services，服务器名称：EC2）的节点有帮助。

[gcping](http://www.gcping.com)：直接访问该网页就会开始测试，稍等一会就会出现你到GCP各个节点的延迟，非常直观。速度最快、延迟最低的那个节点会被提到最前面。

[cloudping](http://www.cloudping.info)：访问网页后点击“HTTP Ping”就会开始测试ping值。

AWS目前有美国、加拿大、德国、冰岛、英国、印度、韩国、新加坡、澳大利亚、日本、巴西、北京有节点。（在国内访问速度都很一般）

### 通过yum源命令来安装wget：
```Bash
yum -y install wget   
```

### 一键测试服务器到国内的速度：

非常的简单，每行一条命令
```Bash
wget https://raw.githubusercontent.com/oooldking/script/master/superspeed.sh
chmod +x superspeed.sh
./superspeed.sh
```

### 一键测试服务器的基本参数：
```Bash
wget -qO- –no-check-certificate https://raw.githubusercontent.com/oooldking/script/master/superbench.sh | bash
```
或者
```Bash
curl -Lso- –no-check-certificate https://raw.githubusercontent.com/oooldking/script/master/superbench.sh | bash
```

### 测试脚本：
```Bash
wget -qO- alicdn.github.io/io.sh | bash
```

### [一键管理脚本](https://www.ubedu.site/archives/528.html)

[逗比](https://doub.ws)的脚本适用环境

CentOS 6+, Debian 6+, Ubuntu 14.04 +

安装：
```Bash
wget -N --no-check-certificate https://raw.githubusercontent.com/ToyoDAdoubi/doubi/master/ssr.sh && chmod +x ssr.sh && bash ssr.sh 
```
控制命令：
```Bash
bash ssr.sh    
```

### [一键安装脚本四合一](https://teddysun.com/486.html/comment-page-1)

秋水逸冰 > 技术 > Shadowsocks 一键安装脚本（四合一）

本脚本适用环境

系统支持：CentOS 6+，Debian 7+，Ubuntu 12+

内存要求：≥128M

使用root用户登录，运行以下命令：
```Bash
wget --no-check-certificate -O shadowsocks-all.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-all.sh
chmod +x shadowsocks-all.sh
./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log
```
若已安装多个版本，则卸载时也需多次运行（每次卸载一种）

使用root用户登录，运行以下命令：
```Bash
./shadowsocks-all.sh uninstall 
```
### [加速一键安装包](https://teddysun.com/489.html)

(BBR加速)使用 root 用户登录，运行以下命令：

```Bash
wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh && chmod +x bbr.sh && ./bbr.sh
```
安装完成后，脚本会提示需要重启 VPS ，输入 y 并回车后重启。

### [提供锐速可用的内核下载](https://www.91yun.co/archives/795)

直接点上面超链接进去

