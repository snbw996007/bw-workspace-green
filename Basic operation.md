# 1.df----du

**df：查看当前已挂载的磁盘空间使用情况**

df -h

![df -h](https://user-images.githubusercontent.com/80690322/149456364-8b85db82-7c6c-4092-8a57-8078c33f88c7.png)

**du：查看当前目录下所有文件夹的空间占用情况**

du -sh

![du -sh](https://user-images.githubusercontent.com/80690322/149456368-0b5d1e8c-6d49-4e92-a75e-61c05a0ea22d.png)

du -h --max-depth=x //目录层级超过x层的不单独统计


# 2.lsof----netstat

**lsof：列出当前系统打开文件的工具**

lsof -i:端口号   //查看端口是否打开

![lsof -i](https://user-images.githubusercontent.com/80690322/149458278-b57fbc6b-a904-46ae-b271-b2c14d57a533.png)

**netstat：显示网络状态**

netstat -atu   //查看开放端口

![netstat -atu](https://user-images.githubusercontent.com/80690322/149458268-51ea8feb-99c6-40c0-bd44-69cf2284f3d6.png)

# 3.fdisk----lsblk

**fdisk：创建和维护分区表的程序**

-l 列出素所有分区表

-u 与 -l 搭配使用，显示分区数目

fdisk -l

![fdisk -l](https://user-images.githubusercontent.com/80690322/149463422-f574308b-ab29-4322-9660-9368406f915f.png)

**lsblk：列出所有可用块设备包括依赖关系的信息，不会列出RAM盘的信息**

![lsblk](https://user-images.githubusercontent.com/80690322/149467284-54ad6b1d-5f6e-4d29-90e9-2ff62308a255.png)

# 4.rpm----yum----deb

**rpm -qa | grep xx**

![rpm -qa](https://user-images.githubusercontent.com/80690322/149689076-7181faf4-f636-4e90-bbb9-42c50cf2c4a6.png)

**rpm -ivh xx:安装命令，可安装多个，空格隔开**

-i:安装
-v:显示详情
-h:安装进度

**rpm -Uvh/-Fvh xx:升级**

-U:没装直接装，装过升级
-F:没装则不装，有低版本升级

**rpm -e xx:卸载**

**yum list install | grep xx**

**dpkg - l | grep xx**

# 5.硬盘相关

**mkfs.vfat  格式化硬盘**

![mkfs vfat](https://user-images.githubusercontent.com/80690322/149727447-ed8e1bb4-3c0e-4afb-ab98-c1a95e070259.png)

