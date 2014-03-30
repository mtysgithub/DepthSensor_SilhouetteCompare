DepthSensor_SilhouetteSmooth
=============================

A smooth algorithm in order to opt depth image of depth sensor

目前基于红外激光散斑技术的深度传感器技术，深度图像在物体的边缘会形成不稳定的噪音信号，表现为一系列高频震动的毛刺。
项目演示了一个简单的基于时间线统计和图像边缘平滑技术的抑躁算法，使得结果图像保持边缘信号稳定，并使之更为平滑。

具体涉及到的算法有：

1. 对不稳定信号进行一定时间尺度上的统计，利用加权函数和阈值设定将不稳定的信号仲裁为一个稳定的信号

2. 利用积分图像对原图像进行形态学滤波，进行腐蚀与膨胀处理以修复凹凸特征

3. 利用中值滤波器改善锯齿边缘的视觉质量


局限：算法的核心目标是优化深度图像的边缘质量，意味着前景物边缘的红外信息与RGB图像将无法精确匹配，算法适用于人物剪影
类项目的图像效果优化。针对前景物体彩色图像的精确抠出和边缘抑噪，需要结合RGB信息与红外信息进行联合分析，算法将在后续
项目中陆续给出。
