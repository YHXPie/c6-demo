# Sever Commands
**目前的服务器列表：**

1. 服务提供商：**Vultr**：149.28.194.64，**地点**：硅谷 _Silicon Valley_
2. N/A
## V2ray
> 原网站：https://tr3.freeair888.club/%E8%87%AA%E5%BB%BAv2ray%E6%9C%8D%E5%8A%A1%E5%99%A8%E6%95%99%E7%A8%8B/

**Ubuntu 16+ / Debian 8+ 系统 v2ray一键部署管理脚本**

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

?> 如果输入安装命令后提示`curl: command not found`，那是因为服务器系统没有自带curl命令，安装一下curl。
?> CentOS系统安装curl：`yum install -y curl`；Debian/Ubuntu系统安装curl：`apt-get install -y curl`
