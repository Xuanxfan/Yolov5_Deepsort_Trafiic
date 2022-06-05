"# Yolov5_Deepsort_Trafiic" 
实现功能：
1. 斑马线检测（opencv）
  斑马线检测（opencv-Canny边缘检测算法）
  1、读取原图像并将图像灰度化
  2、通过高斯滤波去除噪声信息
  3、Canny梯度模
  4、Canny梯度二值化
  5、得到结果
  ![image](https://user-images.githubusercontent.com/54696432/172031453-2fc6ebf7-d4f6-477a-babe-752facc0acd1.png)

2. Yolov5检测行人，车辆，交通信号灯
  
3. Deepsort追踪车辆
  
5. 车辆行驶方向速度检测，超速，闯红灯判断

7. 行人闯红灯判断
8. 
9. 车牌检测

11. 撞线法统计车流量

13. 数据可视化
![image](https://user-images.githubusercontent.com/54696432/172031441-4fa585a3-e2eb-4645-bb32-40bd80946b69.png)

1. 代码中已有全部所需的网络结构

2. 所用数据集如下
基于yolov5s.pt进行训练
BDD100K
https://www.bdd100k.com/
训练结果


车牌识别
CCPD数据集
CCPD(中国城市停车数据集，ECCV)和PDRC(车牌检测与识别挑战)。这是一个用于车牌识别的大型国内的数据集，由中科大的科研人员构建出来的。发表在ECCV2018论文Towards End-to-End License Plate Detection and Recognition: A Large Dataset and Baseline
https://github.com/detectRecog/CCPD

3.运行要求
Python>=3.8
安装所需包
pip install -r requirements.txt
运行main.py
