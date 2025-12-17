# 解决WSL删除文件没有释放空间问题
### 1 进入终端关闭wsl
```bash
wsl --shutdown
```
### 2 进入磁盘目录
```bash
diskpart
```
### 3 选择wsl虚拟磁盘文件，该文件存储wsl所有的文件
```bash
select vdisk file=”E:\WSL\Ubuntu2204\ext4.vhdx”
```
### 4 以只读方式进行
```bash
attach vdisk readonly
```

### 5 压缩磁盘
```bash
compact vdisk
```

### 6 分离虚拟磁盘，让文件不在占用
```bash
detach vdisk
```

原因：windows会自动为vhdx创建虚拟磁盘文件作为wsl的存储，一般文件内存不够时，vhdx后缀的虚拟磁盘文件会自动扩容，但是扩容后，不会自动缩容，所以需要手动压缩，才能释放空间。




