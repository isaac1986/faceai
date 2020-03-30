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

# 输出：4.2.0
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
