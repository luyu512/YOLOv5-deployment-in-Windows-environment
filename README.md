# **YOLOv5保姆级部署教程**

## 第一步：安装anaconda

首先进入清华大学开源软件镜像站
![image](https://github.com/luyu512/yolov5-1-/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202025-03-27%20122142.png)

然后选择适合自己设备的版本（建议版本号大于5.2.0）
![image](https://github.com/luyu512/yolov5-1-/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202025-03-27%20122058.png)

下载并且安装（强烈建议安装在C盘，后续不用再添加环境变量）
![image](https://github.com/luyu512/yolov5-1-/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202025-03-27%20122243.png)

## 第二步： 创建虚拟环境

在终端中输入：

`conda create -n yolo python=3.8`

"yolo"是虚拟环境名称，可自行改变;   “python=3.8”指定python版本为3.8，不建议随意更改，否则后续训练数据集会出错
![image](https://github.com/luyu512/yolov5-1-/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202025-03-27%20125228.png)

## 第三步：从GitHub克隆yolov5文件

项目地址：https://github.com/ultralytics/yolov5

或直接在刚刚创建的虚拟环境中输入以下代码(一定一定要在虚拟环境中操作)：

`git clone https://github.com/ultralytics/yolov5.git`

## 第三步: 安装相关依赖

在第三步基础上，从终端进入刚刚克隆的yolov5文件夹

以我为例：

`cd yolov5`

然后输入命令

`pip install -i https://pypi.tuna.tsinghua.edu.cn/simple -r requirements.txt`
![image](https://github.com/luyu512/yolov5-1-/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202025-03-27%20135706.png)


## 第五步： 用vscode打开文件夹，并且配置Python解释器

进入yolov5文件夹，右键空白区域，选择使用VsCode打开
![image](https://github.com/luyu512/yolov5-1-/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202025-03-27%20135737.png)

进入后，随便打开一个.py文件，在其右下角选择python解释器(如果前面几步无报错，此时选择的python解释器为3.8，且显示虚拟环境名称)
![image](https://github.com/luyu512/yolov5-1-/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202025-03-27%20142055.png)

## 第六步：使用train.py文件训练文件自带模型

在左边文件栏中找到train.py文件，双击进入
在此处将源代码修改如下（博主电脑无GPU，故指定cpu训练）：
![image](https://github.com/luyu512/yolov5-1-/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202025-03-27%20233337.png)

当下方出现如下进度条时，说明训练正常
![image](https://github.com/luyu512/yolov5-1-/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202025-03-27%20145046.png)

## 第七步： 使用detect.py文件检测训练模型

在左边文件栏中找到detect.py文件，双击进入并运行，待程序结束后，会发现左侧文件栏runs文件夹中多出detect子文件夹，双击进入，发现出现两张图片，即为测试图片，打开即可看到被检测的图像
![image](https://github.com/luyu512/yolov5-1-/blob/main/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202025-03-27%20144953.png)

此时，恭喜您，yolov5已经部署至您的电脑上！
