# Linux操作系统（二）
由于大部分电脑的桌面操作系统是Windows，因此想使用Linux操作系统时会犯难。有些人就会直接在Windows电脑上安装Linux系统，将其变为双操作系统。但是这样或多或少会出现一些问题：
>- **分区问题** ：（1）数据丢失：在分区过程中，如果操作不当，会导致原有的Windows分区被格式化，从而导致数据丢失。（2）分区表损坏：若分区表在分区过程中被损坏，可能会导致系统无法启动。
>-  **启动问题** ：（1）引导加载器（Boot Loader）冲突：安装Linux时通常会安装GRUB或LILO作为引导加载器。若安装过程中出现问题，会导致引导加载器损坏，导致系统无法启动。（2）启动项丢失：双操作系统的启动项配置不当，导致无法进入其中一个操作系统。
>- **软件兼容性** ：（1）应用程序的兼容性：某些Windows的应用程序在Linux下可能无法正常运行。

>- 因此，不推荐在Windows电脑上安装双操作系统。同时，我在下面介绍了几种方法，  **可以在Windows电脑上使用Linux操作系统而不需直接安装Linux操作系统**  。

## 1. 虚拟机（virtual machine，VM）--- 推荐
  **使用VM来运行Linux操作系统的具体步骤如下** ：
>- **1. 安装VM软件** ：（1） **VMware Workstation** ：功能强大，支持多种操作系统，但需购买许可证。（2） **Oracle VM VirtualBox** ：开源免费，功能齐全，适合大多数用户。（ **推荐** ）
>- **2. 下载Linux发行版的ISO镜像文件** ：（1）根据需求到Linux发行版的官网选择想要的发行版（不同的发行版有Ubuntu、Fedora、Debian等） （2）下载已选发行版的ISO镜像文件
>- **3. 创建VM** ：（1）启动已安装的VM软件（如VMware workstation，VirtualBox） （2）创建新的VM：---> 点击”Create a New Virtual Machine”  ---> 点击“Installer disc image file (iso)”并选择刚下载的ISO镜像文件 ---> 配置VM的硬件（如内存等）。             ---> 点击“New”按钮 ---> 输入VM名称，选择操作系统和发行版本（Linux，Ubuntu） ---> 配置VM的硬件 ---> 创建完成后，选择VM并点击“Settings”，在“Storage”选项中添加刚下载的ISO镜像文件作为光盘驱动器。
**注**：（2）中创建VM的第一条路径对应的是VMware workstation，创建VM的第二条路径对应VirtualBox）
>- **4. 安装Linux操作系统** ：（1）选择刚刚创建好的VM并点击“Start”按钮  （2）安装Linux： VM启动后会从ISO镜像引导，进入Linux安装界面 ---> 根据指示进行安装 ---> 选择自动分区或者手动分区 ---> 设置用户和密码 ---> 安装完成后会重启VM。
>- **5. 运行Linux操作系统** ：重启VM后就可以使用Linux操作系统了。

**通过以上步骤，可以在Windows电脑上通过虚拟机软件运行Linux操作系统，而无需本地安装Linux，避免对Windows系统造成影响。**

## 2. Windows Subsystem for Linux（WSL） ---不太推荐