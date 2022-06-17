# 添加硬盘 以150G为例

**执行lsblk 查看新添加的硬盘**

![lsblk](https://user-images.githubusercontent.com/80690322/149723531-26a04142-4856-4984-91e5-b166f7d1bcb7.png)

**将新盘做成PV,执行命令  pvcreate /dev/sdb**

![pvcreate devsdb](https://user-images.githubusercontent.com/80690322/149725259-bffec2ad-6f50-4a93-a663-1b7d74d421c0.png)

**查看vg情况，执行命令  vgdisplay**

![vgdisplay](https://user-images.githubusercontent.com/80690322/149725355-abf80e8a-abce-4de7-af3a-51906e5fc60d.png)

**将新盘加入centos  vgextend centos /dev/sdb**

![vgextend](https://user-images.githubusercontent.com/80690322/149725192-a0d45ed5-117d-444e-a38c-3dd2d58b64ec.png)

**查看LV  lvdisplay**

![lvdisplay](https://user-images.githubusercontent.com/80690322/149725622-384e5a8f-d579-4a65-99e6-1a8992b1f7ca.png)

**拉升LV  lvextend -l +100%FREE /dev/centos/var**

![lvextend](https://user-images.githubusercontent.com/80690322/149725943-e6170d06-3ac4-4737-98b1-12d5d9a0fcf0.png)

**再次查看LV  lvdisplay** 

![lv](https://user-images.githubusercontent.com/80690322/149725903-aefb582b-a537-4166-9935-a16070bd2517.png)

**查看文件系统类型  df -lhT**

![df -lhT](https://user-images.githubusercontent.com/80690322/149725673-eefe80dc-97f0-4750-bc4e-1a4d7e1646d6.png)

**刷新文件格式  xfs_growfs /dev/centos/var（xfs格式）或者 resize2fs /dev/centos/var (ext4文件系统)**

![xfs_growfs](https://user-images.githubusercontent.com/80690322/149725408-a919beb2-7b9a-47b3-9a7d-087234b772ae.png)

**df -h （前后对比）**

![df](https://user-images.githubusercontent.com/80690322/149726093-8a9b2baa-3913-436f-b635-eb39ab788ecc.png)

![df -h](https://user-images.githubusercontent.com/80690322/149725537-6bdc3c40-d395-4669-b08f-2841e150c17a.png)
