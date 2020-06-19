# my-model-zoo
存放我训练的有趣的机器学习模型




模型一： 基于keras框架的迁移学习，用于识别两种花卉（玫瑰(rose)和向日葵(sunflower))


 基本信息：使用MobileNet预训练权重，训练最后20层，并在最后两层添加全连接层（因为数据量较小，添加两个Dense层可以学习到更细致的图像信息）并使用softmax函数激活，使用Adam算法做梯度优化，用交叉熵函数计算损失。输入图像尺寸为（224 * 224）经典尺寸。训练数据来源为Kaggle。
 
 训练代码：https://github.com/sheng-zhong/my-model-zoo/blob/master/transfer_learning.ipynb
 
 模型地址： https://pan.baidu.com/s/1xv5oBjhcBAHpchuaEXtTdg
 提取码：hz8h
 
 数据地址： https://pan.baidu.com/s/11tRJYjLFzfetT7OEXig33w
 提取码：2pt9

![image](https://github.com/sheng-zhong/my-model-zoo/blob/master/results/transfer/result.png)

模型二：基于darknet的检测模型，看见楼下业主维权，训练了个用于检测横幅（banner）在图像中的位置的模型。


基本信息：算法基于YOLOV4，我更改了其yolo图层和卷积图层以及输出层、输入层、由于数据是自己收集标注的，所以数量较少。因此在图像增强上添加了一些原本不在官方内容中的方法，数据来源为自己标注，已经开源。

训练过程的损失：https://github.com/sheng-zhong/my-model-zoo/blob/master/results/darknet/chart_yolov4-voc-banner.png

模型地址：https://pan.baidu.com/s/1anBA-X3L9QtgWHkvRk9qEQ    提取码：nb73

数据地址：https://pan.baidu.com/s/1cMt4DGvNUvmkIVuaCMs0ww    提取码：vgzr

![image](https://github.com/sheng-zhong/my-model-zoo/blob/master/results/darknet/predictions.jpg)


模型三：使用对抗生成网络（GANs）去生成逼真的人脸数据
