# 1.df----du

**df：查看当前已挂载的磁盘空间使用情况；

df -h

![df -h](https://user-images.githubusercontent.com/80690322/149456364-8b85db82-7c6c-4092-8a57-8078c33f88c7.png)

**du：查看当前目录下所有文件夹的空间占用情况;

du -sh

![du -sh](https://user-images.githubusercontent.com/80690322/149456368-0b5d1e8c-6d49-4e92-a75e-61c05a0ea22d.png)

du -h --max-depth=x //目录层级超过x层的不单独统计


# 2.lsof----netstat

**lsof：列出当前系统打开文件的工具

lsof -i:端口号   //查看端口是否打开

![lsof -i](https://user-images.githubusercontent.com/80690322/149458278-b57fbc6b-a904-46ae-b271-b2c14d57a533.png)

**netstat：

netstat -atu   //查看开放端口

![netstat -atu](https://user-images.githubusercontent.com/80690322/149458268-51ea8feb-99c6-40c0-bd44-69cf2284f3d6.png)

# 3.fdisk：创建和维护分区表的程序

fdisk -l

![fdisk -l](https://user-images.githubusercontent.com/80690322/149463422-f574308b-ab29-4322-9660-9368406f915f.png)
