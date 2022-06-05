"# Yolov5_Deepsort_Trafiic" 

实例视频：
Yolov5_Deepsort_Trafiic/demo (1).mp4

实现功能：

1. 斑马线检测（opencv）

    斑马线检测（opencv-Canny边缘检测算法）
  
    1、读取原图像并将图像灰度化
  
    2、通过高斯滤波去除噪声信息
  
    3、Canny梯度模
  
    4、Canny梯度二值化
  
    5、得到结果
  
  ![image](https://user-images.githubusercontent.com/54696432/172031700-83a86a7b-bbc8-41fb-82e7-23c3e3e25635.png)
  ![image](https://user-images.githubusercontent.com/54696432/172031706-f3c272a0-9757-48cd-be6f-1fad75cdb2ed.png)
  ![image](https://user-images.githubusercontent.com/54696432/172031712-4522275c-d3da-4cd9-bf45-38eb5c02c012.png)


2. Yolov5检测行人，车辆，交通信号灯
  ![image](https://user-images.githubusercontent.com/54696432/172031724-64b584ac-37b5-471e-b783-fb9815986be4.png)
  ![image](https://user-images.githubusercontent.com/54696432/172031730-e8429b65-99a8-4c23-b728-f899b1450b4c.png)

3. Deepsort追踪车辆

4. 车辆行驶方向速度检测，超速，闯红灯判断
  ![image](https://user-images.githubusercontent.com/54696432/172031734-8b691c3c-1205-47e6-b816-8c54fcc22278.png)

5. 车辆闯红灯判断

6. 车牌检测

7. 撞线法统计车流量

8. 数据可视化检测目标统计，车流量统计，车速区间统计，闯红灯抓拍，超速抓拍)
  具体例子可见Yolov5_Deepsort_Trafiic/inference/output/01/



PS：
  1. 代码中已有全部所需的网络结构

  2. 所用数据集如下

基于yolov5s.pt进行训练

BDD100K

https://www.bdd100k.com/

训练结果
![image](https://user-images.githubusercontent.com/54696432/172031921-edf666ec-4af6-49f0-b46b-e807e59a07dc.png)
![image](https://user-images.githubusercontent.com/54696432/172031924-43d672a5-6bf3-4f89-9992-9613729aef4e.png)


车牌识别

CCPD数据集

CCPD(中国城市停车数据集，ECCV)和PDRC(车牌检测与识别挑战)。这是一个用于车牌识别的大型国内的数据集，由中科大的科研人员构建出来的。发表在ECCV2018论文Towards End-to-End License Plate Detection and Recognition: A Large Dataset and Baseline

https://github.com/detectRecog/CCPD

3.运行要求

Python>=3.8

安装所需包

pip install -r requirements.txt

运行main.py

可能的改进：

1.可以增加Ui界面，所有的条件都可以通过图形界面来设定，结果与图表的展示也可以更加直观。可以大大提高该系统的易用性，实用性与用户友好程度

2.使用BDD100K数据集训练的模型对交通信号灯的识别效果较为一般，可以增加训练一个CNN之类的网络用于专门识别红绿灯，效果应该会更好

3.当前的测速是一个单纯的像素到距离的线性映射，实际上由于监控镜头是固定的，我们可以计算出二维图片到三维世界的映射关系，这样得到的车速才更严谨可靠
