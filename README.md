# my-model-zoo
存放我训练的有趣的机器学习模型




模型一： 基于keras框架的迁移学习，用于识别两种花卉（玫瑰(rose)和向日葵(sunflower))


 基本信息：使用MobileNet预训练权重，训练最后20层，并在最后两层添加全连接层（因为数据量较小，添加两个Dense层可以学习到更细致的图像信息）并使用softmax函数激活，使用Adam算法做梯度优化，用交叉熵函数计算损失。输入图像尺寸为（224 * 224）经典尺寸。训练数据来源为Kaggle。
 
 训练代码：https://github.com/sheng-zhong/my-model-zoo/blob/master/transfer_learning.ipynb
 
 模型地址： https://pan.baidu.com/s/1xv5oBjhcBAHpchuaEXtTdg      提取码：hz8h
 
 数据地址： https://pan.baidu.com/s/11tRJYjLFzfetT7OEXig33w      提取码：2pt9

![image](https://github.com/sheng-zhong/my-model-zoo/blob/master/results/transfer/result.png)

模型二：基于darknet的检测模型，看见楼下业主维权，训练了个用于检测横幅（banner）在图像中的位置的模型。


基本信息：算法基于YOLOV4，我更改了其yolo图层和卷积图层以及输出层、输入层、由于数据是自己收集标注的，所以数量较少。因此在图像增强上添加了一些原本不在官方内容中的方法，数据来源为自己标注，已经开源。

训练过程的损失：https://github.com/sheng-zhong/my-model-zoo/blob/master/results/darknet/chart_yolov4-voc-banner.png

模型地址：https://pan.baidu.com/s/1anBA-X3L9QtgWHkvRk9qEQ    提取码：nb73

数据地址：https://pan.baidu.com/s/1cMt4DGvNUvmkIVuaCMs0ww    提取码：vgzr

![image](https://github.com/sheng-zhong/my-model-zoo/blob/master/results/darknet/predictions.jpg)


模型三：使用对抗生成网络（GANs）去生成逼真的人脸数据


基本信息：使用人脸数据训练生成器和检测器，由于算力要求太高，数据量也比较有限（3000张左右的人脸数据），所以自己自己训练的权重产生的人脸效果并不好，训练过程可以看到生成的人脸回越来越清晰（不过还是很古怪的人脸），输入输出图像的分辨率为 96 * 96。再清晰点就很难等了...使用Nvidia的预训练权重可以生成非常清晰，并且一般人分辨不了真伪的人脸图像，这些人脸是不存在的或者说是没有版权的。可以应用再一些UI设计上。数据来源为Kaggle。

训练过程代码：https://github.com/sheng-zhong/my-model-zoo/blob/master/GANs.ipynb

自己训练的模型：https://pan.baidu.com/s/1bmgAbiNTe4HNokN_Ak41OA      提取码：ghrp

Nvidia的开源模型：https://pan.baidu.com/s/1bmgAbiNTe4HNokN_Ak41OA      提取码：ghrp

数据地址：https://pan.baidu.com/s/1N4pB9b0d_0n9TYobbMxNOQ      提取码：00l8

第0到3个epoch生成器的变化：
![image](https://github.com/sheng-zhong/my-model-zoo/blob/master/results/gans/face.png)

生成器模型最终可以生成的图像：
![image](https://github.com/sheng-zhong/my-model-zoo/blob/master/results/gans/face.png)

nvidia预训练模型最终生成的人脸：
![image](https://github.com/sheng-zhong/my-model-zoo/blob/master/results/gans/face.png)


模型四：用DQN（强化学习+深度学习）的Q-table算法让AI学会玩游戏。

基本信息：
