# my-model-zoo
存放我训练的有趣的机器学习模型

模型一： 基于keras框架的迁移学习，用于识别两种花卉（玫瑰(rose)和向日葵(sunflower))

 基本信息：使用VGG16预训练权重，训练最后20层，并在最后两层添加全连接层（因为数据量较小，添加两个Dense层可以学习到更细致的图像信息）并使用softmax函数激活，使用Adam算法做梯度优化，用交叉熵函数计算损失。输入图像尺寸为（224 * 224）经典尺寸。
 
 效果图： https://github.com/sheng-zhong/my-model-zoo/tree/master/results/transfer
 模型地址： https://pan.baidu.com/s/1xv5oBjhcBAHpchuaEXtTdg   提取码：hz8h
