# Sever Commands
**目前的服务器列表：**

1. 服务提供商：**Vultr**：XXX.XXX.XXX.XX，**地点**：X国，X州，XX _Some Place_
2. 服务提供商：**RackNerd**：23.94.94.166，**地点**：美国，佐治亚州，亚特兰大 _Atlanta_
- - -
# V2ray
!> 原网站：（寄了已经）

### Ubuntu 16+ / Debian 8+ 系统 v2ray一键部署管理脚本

安装：

```
source <(curl -sL https://multi.netlify.app/v2ray.sh) --zh
```

升级(保留配置文件更新)：

```
source <(curl -sL https://multi.netlify.app/v2ray.sh) -k
```

卸载：

```
source <(curl -sL https://multi.netlify.app/v2ray.sh) --remove
```

?> 如果输入安装命令后提示`curl: command not found`，那是因为服务器系统没有自带curl命令。
```
# CentOS系统安装curl：
yum install -y curl

# Debian/Ubuntu系统安装curl：
apt-get install -y curl
```
