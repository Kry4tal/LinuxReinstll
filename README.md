# LinuxReinstall
Backup
# USE
wget --no-check-certificate -qO netre.sh 'https://git.io/NetRe' && chmod a+x netre.sh
## Debian/Ubuntu:
apt-get install -y xz-utils openssl gawk file
 
## RedHat/CentOS:
yum install -y xz openssl gawk file

## 使用默认镜像全自动安装
bash netre.sh -d 8 -v 64 -a
 
## 使用自定义镜像全自动安装
bash netre.sh -c 6.9 -v 64 -a --mirror 'http://mirror.centos.org/centos'
 
### 以下示例中,将X.X.X.X替换为自己的网络参数.
#### --ip-addr :IP Address/IP地址
#### --ip-gate :Gateway   /网关
#### --ip-mask :Netmask   /子网掩码
 
## 使用自定义镜像自定义网络参数全自动安装
### bash netre.sh -u 16.04 -v 64 -a --ip-addr x.x.x.x --ip-gate x.x.x.x --ip-mask x.x.x.x --mirror 'http://archive.ubuntu.com/ubuntu'
 
## 使用自定义网络参数全自动dd方式安装
### bash netre.sh --ip-addr x.x.x.x --ip-gate x.x.x.x --ip-mask x.x.x.x -dd 'https://moeclub.org/get-win7embx86-auto'
 
## 使用自定义网络参数全自动dd方式安装存储在谷歌网盘中的镜像(调用文件ID的方式)
### bash netre.sh --ip-addr x.x.x.x --ip-gate x.x.x.x --ip-mask x.x.x.x -dd "$(echo "1cqVl2wSGx92UTdhOxU9pW3wJgmvZMT_J" |xargs -n1 bash <(wget --no-check-certificate -qO- 'https://moeclub.org/get-gdlink'))"
 
## 使用自定义网络参数全自动dd方式安装存储在谷歌网盘中的镜像
### bash netre.sh --ip-addr x.x.x.x --ip-gate x.x.x.x --ip-mask x.x.x.x -dd "$(echo "https://drive.google.com/open?id=1cqVl2wSGx92UTdhOxU9pW3wJgmvZMT_J" |xargs -n1 bash <(wget --no-check-certificate -qO- 'https://moeclub.org/get-gdlink'))"
