# OpenCV环境搭建 #

本文将介绍OpenCV在Python3.x上的实现，Windows版。

## Windows版环境搭建 ##

> 系统环境：windows 7 + python 3.8.2 + OpenCV 4.2.0


### 一、安装python ###



### 二、安装numpy模块 ###

根据上文提示，现在我们已经正确安装了python和pip（安装和管理python包的工具），在正式安装OpenCV之前，首先我们要安装numpy模块。
numpy：是一个定义了数值数组和矩阵类型和它们的基本运算的语言扩展，OpenCV引用了numpy模块，所以安装OpenCV之前必须安装numpy。

> pip3 install numpy

命令窗体显示：

Installing collected packages: numpy

Successfully installed numpy-1.18.2

说明已经安装成功。


### 三、安装OpenCV ###
同样安装OpenCV模块和numpy方式类似。

https://pypi.tuna.tsinghua.edu.cn/simple/opencv-python/ 下载opencv_python-4.2.0.32-cp38-cp38-win_amd64.whl

> pip3 install opencv_python-4.2.0.32-cp38-cp38-win_amd64.whl

窗体显示：

Installing collected packages: opencv-python

Successfully installed opencv-python-4.2.0.32

说明安装成功。

### 四、运行OpenCV ###
到此，我们的环境配置已经完成了，终于到了可以撸代码的时刻了，想想还有一点小激动呢。


``` python
import cv2

print(cv2.__version__)

# 输出：3.4.1
```
上面我们简单的打印了OpenCV的版本号，如果能正常输出不报错，说明我们已经把OpenCV的python环境搭建ok了。

什么？感觉还不过瘾，那就来撸一张图，用OpenCV把它展示出来，代码如下：
``` python
import cv2

filepath = "img/meinv.png"
img = cv2.imread(filepath)
cv2.namedWindow('Image')
cv2.imshow('Image', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

展示效果如图：![正在加载图片](https://raw.githubusercontent.com/vipstone/opencvLab/master/res/show-meinv.png)


	
----------
## Linux版环境搭建 ##

>Ubuntu 18.04
>Python 3.6.5
>Pip 10.0.1
>Numpy 1.14.3
>OpenCV 3.4.0

Ubuntu有一个好处就是内置Python环境，不需要像Windows那样在为Python环境折腾了，但要注意的是Ubuntu本身自带的apt-get和安装的pip的数据源是国外的，所以使用起来都很慢，一定要把apt-get和pip的数据源更换成国内的，请移步到：[《Ubuntu apt-get和pip源更换》](http://www.cnblogs.com/vipstone/p/9038023.html)

### 正式安装 ###
根据上面的提示，你已经配置好了开发环境，现在需要正式安装了，当然Ubuntu的安装也比Windows简单很多，只需要使用pip安装包，安装相应的模块即可。

#### 安装Numpy ####
使用命令：pip3 install numpy

使用命令：python3，进入python脚本执行环境，输入代码查看numpy是否安装成功，以及numpy的安装版本：
```
import numpy 

numpy.__version__
```
正常输入版本号，证明已经安装成功。

如图：![](http://icdn.apigo.cn/numpy-setup-success.png)

#### 安装OpenCV ####
OpenCV的安装在Ubuntu和numpy相似，使用命令：
>pip3 install opencv-python

使用命令：python3，进入python脚本执行环境，输入代码查看OpenCV版本：
```
import cv2 

cv2.__version__
```
正常输出版本号，证明已经安装成功。

# 常见错误 #

错误一、python3: Relink `/lib/x86_64-linux-gnu/libudev.so.1` with `/lib/x86_64-linux-gnu/librt.so.1` for IFUNC symbol `clock_gettime`
Segmentation fault (core dumped)

解决方案：apt install python3-opencv


----------

