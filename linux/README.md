# 添加内存交换区(swap)

### 1.创建1G的file
```shell
dd if=/dev/zero of=/mnt/1GB.swap bs=1M count=1024
```

### 2.格式化为swap file
```shell
mkswap /mnt/1GB.swap
```

### 3.把swap file加入到系统中
```shell
swapon /mnt/1GB.swap
```

### 4.将swap永久添加
在/ect/fstab中加入新的Swap分区
```shell
vi /etc/fstab
```
在最后加入下列内容 /mnt/1GB.swap none swap sw 0 0

### 5.查看
```shell
free -m
```
