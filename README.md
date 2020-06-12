# Brest-Cancer-Detection
### 1. Introduction
这次的数据集既包括文本又包括图片，我们要根据这些数据对乳腺癌病人的分子亚型进行分类，共有四类。

### 2. Method
主要思路： 分类以图片数据为主，由于每个病人的病理图片数量不一，单凭图片可能存在分不了类的情况。在此种情况下，我们引入文本信息进行辅助分类。

图片处理方法：CNN

文本处理方法：决策树

我们采用了两种网络结构训练图片，VGG16和ResNet18。batch_size大小设置为16，跑了20个epoch。对于VGG16，20个epoch结束后，acc不到0.5。而对于ResNet18，20个epoch之, acc可以达到0.97。在test阶段，将采用ResNet18 model。

