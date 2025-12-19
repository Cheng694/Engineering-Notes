# 解决安装Tex Live卡在卡在running package-specific postactions

卡在 running package-specific postactions 主要是gui的问题

### 1 下载
官方镜像
http://mirror.ctan.org/systems/texlive/Images/texlive2025.iso
下载速度慢，采用国内镜像
清华大学（北京）：https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/texlive/Images/texlive2025.iso
上海交通大学（上海）：https://mirrors.sjtug.sjtu.edu.cn/ctan/systems/texlive/Images/texlive2025.iso

### 2 Windows下的 no gui 安装过程
下载的镜像如图
![alt text](image.png)

右键，把镜像装载如下
![alt text](image-1.png)

点击打开
![alt text](image-2.png)

记住装载路径
![alt text](image-3.png)

以管理员的身份启动终端命令
![alt text](image-4.png)

进入装载盘
```bash
F:
```
![alt text](image-5.png)

查看目录
```bash
dir
```
![alt text](image-6.png)

启动 no gui 安装
```bash
install-tl-windows.bat --no-gui
```
![alt text](image-8.png)
![alt text](image-7.png)

输入D改变安装路径
![alt text](image-9.png)
![alt text](image-10.png)

选择1，然后更改路径例如
```bash
E:/texlive/2025
```
![alt text](image-11.png)

输入R返回
![alt text](image-12.png)

然后输入I进行安装
![alt text](image-13.png)

安装成功
![alt text](image-14.png)

