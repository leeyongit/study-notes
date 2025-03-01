# rabbitmq 基础安装使用

#### 1 准备：
```sh
yum install
build-essential openssl openssl-devel unixODBC unixODBC-devel
make gcc gcc-c++ kernel-devel m4 ncurses-devel tk tc xz
```
#### 2 下载：
```
wget www.rabbitmq.com/releases/erlang/erlang-18.3-1.el7.centos.x86_64.rpm
wget http://repo.iotti.biz/CentOS/7/x86_64/socat-1.7.3.2-5.el7.lux.x86_64.rpm
wget www.rabbitmq.com/releases/rabbitmq-server/v3.6.5/rabbitmq-server-3.6.5-1.noarch.rpm
```
#### 3 配置 vim /etc/hosts 以及 /etc/hostname (Linux防火墙)
```
127.0.0.1 rabbitmq
```
/etc/hostname 如下 写个rabbitmq
linux命令 hostname 显示 rabbitmq 可能存在没生效。

#### 4 配置文件：
```
vim /usr/lib/rabbitmq/lib/rabbitmq_server-3.6.5/ebin/rabbit.app
```
比如修改密码、配置等等，例如：loopback_users 中的 <<"guest">>,只保留guest
服务启动和停止：
启动 rabbitmq-server start &
停止 rabbitmqctl app_stop

#### 5 管理插件：rabbitmq-plugins enable rabbitmq_management
 访问地址：http://ip:15672/

