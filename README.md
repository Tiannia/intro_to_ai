



# 图像风格迁移

### 一、**选题背景**

图像风格迁移是指利用计算机将一个图像以不同的图像风格呈现出来。传统的图像风格迁移算法主要为对图像的局部特征进行建模分析，改变待迁移的图像使其更好符合建立的模型。这种算法的局限性在于单个模型只能对某一种风格或者某一个场景进行迁移。近年来随着神经网络的发展，机器在某些视觉感知的关键领域，比如物体和人脸识别等有着接近于人类甚至超越人类的的表现。本次课题我们所研究的基于神经网络的图像风格迁移利用神经网络将图像特征提取出来，并与任意图片内容结合，从而得到质量较高的风格迁移图像。

### 二、**相关研究综述**

第一个基于神经网络的图像风格迁移算法在2015年由Gatys等人在《A Neural Algorithm of Artistic Style》与《Texture Synthesis Using Convolutional Neural Networks》中提出。Gatys等人给出了一个基于卷积神经网络（CNN）的纹理合成和图像识别的算法。2017年Dumoulin等人在《A Learned Representation for Artistic Style》中给出了一种利用单个卷积神经同时学习多个风格的方法，从而实现实时图像风格迁移以及视频风格迁移。

### 三、**拟解决的问题和研究内容**

（1）如何描绘图片的风格与内容特征

通过选取合适的卷积神经网络模型（如VGG-16、VGG-19），将训练集经过神经网络，获取模型不同层的输出来表示图片的内容特征和风格特征。

（2）计算内容损失和风格损失

将内容图片输入神经网络获取内容层输出的内容特征矩阵，通过特定公式计算每层的内容损失。将风格图片输入神经网络，利用不同层的Gram矩阵计算风格特征，通过风格损失函数关联计算出风格损失。

（3）风格迁移

选取合适损失函数，对内容损失和风格损失加权求和，最小化内容图片与生成图片某层内容表示之间的差距以及风格图片与生成图片多层风格表示之间的差距。

（4）训练图像生成模型

下载数据集，向网络中输入噪声图片进行训练，利用损失函数不断计算调整，理想情况下内容损失和风格损失都随着训练不断下降，最终完成图像生成模型的训练。

### **四、可行性分析**

小组成员具备的能力和初步分工：

由于各成员都是初学者，需要不断地进行相关文献的阅读以及课程项目的研究。

xxx负责查文献和理论研究部分，xxx负责代码部分。

已有的学习资源：

师兄师姐的优秀作品、B站风格迁移学习视频、Github风格迁移项目。

优质的GitHub项目例如：

- https://github.com/luanshiyinyang/DeepLearningProject/tree/master/NeuralStyle    
- https://github.com/anishathalye/neural-style 

可借助的工具、开源代码：pycharm、tensorflow、PaddlePaddle、Keras、OpenCV

### **五、计划进度安排**

3月20日至3月26日，完成选题并分配好小组成员任务。

3月27日至4月5日，查阅文献资料，并完成开题报告。

4月6日至4月20日，小组成员相互合作，写出基本代码框架。

4月21日至4月30日，完善代码，基本完成项目。

5月1日至5月10日：完成项目进展报告。

5月11日至5月20日，测试代码，并修改bug。

5月21日至5月31日，完成项目期末报告和项目汇报视频。

### 六、**参考文献**

[1]《A Neural Algorithm of Artistic Style》 [https://arxiv.org/pdf/1508.06576.pdf]

[2]《Texture Synthesis Using Convolutional Neural Networks》

[3]《A Learned Representation for Artistic Style》

Deep Leaning and CNN website:

- http://neuralnetworksanddeeplearning.com/chap6.html

- https://e2eml.school/how_convolutional_neural_networks_work.html	



### **七、图片实例**

> Source

![source](https://github.com/Tiannia/intro_to_ai/blob/main/img-folder/content.jpg)

> Style

![style](https://github.com/Tiannia/intro_to_ai/blob/main/img-folder/style.jpg)

> Result

![result](https://github.com/Tiannia/intro_to_ai/blob/main/img-folder/20.jpg)