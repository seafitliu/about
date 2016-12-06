# Linux引导过程 #
## 第一个程序 - bootloader
### GRUB Legacy
#### 核心镜像core.img、配置grub.cfg及配套工具
![grub0.97](./doc/grub0.97.PNG)

![grub0.97-2](./doc/grub0.97-2.PNG)

## 编译内核
	apt-get source linux-image-$(uname -r)		#下载当前版本内核
## vmlinuz可引导的、压缩的内核（vmlinux未压缩）
	make zImage		#小内核，自带gzip解压代码，老的zImage解压缩内核到低端内存(第一个640K)
    make bzImage	#大内核，自带gzip解压代码，bzImage解压缩内核到高端内存(1M以上)
## initrd.img
## System.map内核符号表
	cat /boot/System.map | grep do_fork		#查看do_fork地址
## 初始化系统 - sysvinit
- service

        service 服务名 start/stop/status... #/etc/init.d/服务文件脚本（服务名）

- chkconfig

## 初始化系统 - systemd
## 内核信息
	cat /proc/cmdline
	cat /proc/kallsyms
