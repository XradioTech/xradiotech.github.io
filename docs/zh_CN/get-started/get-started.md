
![](../../images/XRADIOTECHLOGO.png)

[[English]](index-en.md)

此文档旨在指导芯之联无线MCU产品开发者从零开始搭建开发所必须的软硬件开发环境，为开发工作做好准备，并指导其在某一指定平台完成SDK下载，工具安装，工程创建，编译，打包，烧录等一系列流程步骤。

|<img src="../../images/note-white.png" width=15/>  注意|
|----|
|该文档中提到的一系列步骤具有普适性，适用于XR808，XR872等各无线MCU SDK平台，示例为了方便选取其一，其他平台需要根据其硬件及软件定义灵活处理|

|<img src="../../images/note.png" width=15/>  注意|
|----|
|该文档中提到的一系列步骤具有普适性，适用于XR808，XR872等各无线MCU SDK平台，示例为了方便选取其一，其他平台需要根据其硬件及软件定义灵活处理|
![](../../images/note.png)注意

# 概述

# 准备工作
* 硬件
    * 一块XR872开发板
    * 一根USB转UART线 (建议采用CH340芯片平台)
    * PC (Windows，Linux或MacOS)

* 软件
    * 工具链及编译工具(gcc, make等)
    * git工具
    * 代码编辑器(VSCode，Ultraedit，Vim等)

连接示意图如下：  
![](../../images/PC2MCU.png)

# 了解硬件
请点击下方链接，了解有关具体开发板的详细信息。  
     * [XR872_EVB_IO](xr872_evb_io.md)
     * [XR872_EVB_AI](xr872_evb_AI.md)
     * [XR808_EVB_IO](xr808_evb_io.md)

# 搭建环境
## Linux平台搭建
以Ubuntu为代表系统说明如下：
1. 打开终端窗口，安装开发相关工具，在终端窗口输入以下命令
```
sudo apt-get install cmake git python python-pip vim
```
2. 创建工作目录并下载SDK
```
mkdir xradiotech
cd xradiotech
git clone https://github.com/XradioTech/xradio-skylark-sdk.git
```
此时芯之联无线MCU SDK将会下载到xradiotech的目录下，仓库名为xradio-skylark-sdk
3. 创建工具目录，并下载gcc工具
```
cd xradiotech
mkdir tools
cd tools
wget https://launchpad.net/gcc-arm-embedded/4.9/4.9-2015-q2-update/+download/gcc-arm-none-eabi-4_9-2015q2-20150609-linux.tar.bz2
tar -xf gcc-arm-none-eabi-4_9-2015q2-20150609-linux.tar.bz2
```
## Windows平台搭建
1. 安装Cygwin工具
     * 从Cygwin官方网站下载Cygwin终端setup-x86.exe
     * 运行setup-x86.exe安装Cygwin工具包（**注意：安装路径不要包含中文路径或者空格**）
     * 在安装包选项选择想要安装的工具包（**cmake, git, wget, binutils， python, python-pip， zip, unzip, vim**等）
2. 运行Cygwin Terminal进入到终端程序，进入到工程目录（自己选择），创建工程目录，并下载SDK
```
mkdir xradiotech
cd xradiotech
git clone https://github.com/XradioTech/xradio-skylark-sdk.git
```
此时芯之联无线MCU SDK将会下载到xradiotech的目录下，仓库名为xradio-skylark-sdk
3. 创建工具目录，并下载gcc工具
```
cd xradiotech
mkdir tools
cd tools
wget https://launchpad.net/gcc-arm-embedded/4.9/4.9-2015-q2-update/+download/gcc-arm-none-eabi-4_9-2015q2-20150609-win32.zip
unzip -o gcc-arm-none-eabi-4_9-2015q2-20150609-win32.zip
```

|<img src="../../images/note-white.png" width=15/>  注意|
|----|
|如果wget和unzip命令执行失败，请点击上面的链接直接下载并解压缩|

## 编译示例工程

## 烧录固件

## 调试使用

## 创建新工程

## 配置新工程

## 工程小技巧
