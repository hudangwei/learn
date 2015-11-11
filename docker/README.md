#centos6.5 安装docker

##1.查看系统版本号
```shell
lsb_release -a
```

##2.查看内核版本
```shell
uname -a
```

##3.yum方式升级内核（因为Docker推荐使用3.8以上内核）
```shell
rpm --import https://www.elrepo.org/RPM-GPG-KEY-elrepo.org
rpm -Uvh http://www.elrepo.org/elrepo-release-6-6.el6.elrepo.noarch.rpm
yum --enablerepo=elrepo-kernel install kernel-lt -y
```

##4.修改内核启动项
```shell
vi /etc/grub.conf 
``` 
新安装的内核一般在第一个,这里把default = 1 改为 default = 0

##5.重启系统
```shell
reboot
```

##6.查看内核信息
```shell
uname -r
```

##7.安装docker
```shell
yum install -y epel-release
yum install -y docker-io

docker version

docker -d
```
