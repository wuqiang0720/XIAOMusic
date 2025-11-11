### VMare 安装虚拟机设置桥接网络,并且安装vmtool，然后共享本地的Music文件夹给虚拟机如下:
<img width="723" height="472" alt="image" src="https://github.com/user-attachments/assets/ed7fc40f-e3b1-4801-ab87-5598031b7bdf" />

```
sudo apt update
sudo apt install -y open-vm-tools
sudo systemctl enable --now vmtoolsd.service
sudo systemctl enable --now vgauth.service
systemctl status vmtoolsd.service
```
<img width="726" height="793" alt="image" src="https://github.com/user-attachments/assets/6903d535-56ab-48a5-80f8-64f936c0a9a7" />
```
ubuntu@ubuntu:~$ df -h /mnt/hgfs
Filesystem                         Size  Used Avail Use% Mounted on
vmhgfs-fuse                        159G  113G   47G  71% /mnt/hgfs
ubuntu@ubuntu:~$ ll /mnt/hgfs/
total 13
dr-xr-xr-x 1 root root 4192 Nov 11 01:47 ./
drwxr-xr-x 4 root root 4096 Nov 11 01:01 ../
drwxrwxrwx 1 root root 4096 Oct 16 08:15 Music/
```

### 用docker-compose安装容器
```
docker-compose up -d
```
