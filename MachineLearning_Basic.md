[图片本地路径](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images)

# 一、机器学习基础

## 1. 机器学习的概念

![image-20230228192505873](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102107647.png)

特征间的相关性较强时，可以省略掉其中某个特征

![image-20230228192825383](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102107004.png)

![image-20230228193252527](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102108883.png)

![image-20230228193428286](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102108406.png)

![image-20230228193644422](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102108656.png)

![image-20230228193829252](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102108643.png)

![image-20230228193912238](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102108593.png)

![image-20230302160222891](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102108556.png)

![image-20230302160742146](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102111923.png)

## 2. 机器学习的分类

![image-20230302160848905](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102111258.png)

![image-20230302161113568](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102111905.png)

![image-20230302161224907](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102112918.png)

![image-20230302161247882](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102112067.png)

降维：在多个特征中选取几个重要特征，就会从高维变成低维（主成分分析PCA）

![image-20230302161537567](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102112586.png)



## 3. 机器学习的背景知识

![image-20230302162056194](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102112260.png)

高等数学 > 概率论 > 线性代数 > 数理统计 > 信息论

![image-20230302162229440](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102112779.png)



# 二、有监督学习

## 1. 朴素贝叶斯

![image-20230302162831038](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102112737.png)

![image-20230302162922138](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102112436.png)

![image-20230302163211018](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102112955.png)

![image-20230302163338358](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102113389.png)

![image-20230302163613872](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102113560.png)

---

![image-20230302163918767](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102113689.png)

![image-20230302164006119](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102113328.png)

![image-20230302164217727](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102114470.png)

语料库的规则和自己定义的规则 ---> 预测结果

---

![image-20230302164533966](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102114432.png)

![image-20230302164619223](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102114474.png)

![image-20230302164650534](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102114516.png)

 朴素不是为了提升算法的性能，而是不得已的假设，不然就会是一连串的条件概率

![image-20230302165030966](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102114718.png)

![image-20230302165337117](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102114494.png)

![image-20230302165429597](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102114045.png)

![image-20230302165516342](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102114438.png)



## 2. 决策树算法

![image-20230302190100062](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102114773.png)

- 内部节点：一个特征或属性
- 叶节点：一个类

先后顺序不同的结果是不一样的

![image-20230302190235273](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102114671.png)

![image-20230302190342594](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102114470.png)

---

### 2.1 ID3

![image-20230302190420152](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102114441.png)

---

![image-20230302190513601](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102114836.png)

![image-20230302190800025](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102115253.png)

原始数据：【⚪⚪⚪⚪⚪🔺🔺🔺🔺🔺】

第一种分类结果：【⚪⚪⚪⚪⚪】【🔺🔺🔺🔺🔺】 ---> 信息增益比较大

第二种分类结果：【⚪⚪⚪🔺🔺】【⚪⚪🔺🔺🔺】 ---> 信息增益比较小

---

**例子**

![image-20230302191127656](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102115752.png)

![image-20230302191224472](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102115686.png)

![image-20230302191234624](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102115783.png)

![image-20230302191336624](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102115872.png)

信息增益：g(D, A) = 0.971 - 0.8897 = ...

---

![image-20230302191420864](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102115994.png)

 假设信息增益分别是：有工作--->0.2，有房子--->0.17，有信用--->0.09，我们会选择信息增益最大的特征作为当前的决策节点（有工作），先把有工作当作树的根节点，对数据进行分类，再去求其他特征在分好类的子集中的信息增益，依次迭代作为根节点，再去分子集....



如果以编号作为特征进行分类，就会是一个编号一个类别，它的信息熵 = (1/1) * log(1/1) * 14 = 0，分类太好了？ ×

---

### 2.2 C4.5

![image-20230302194204510](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102115008.png)

![image-20230302194247846](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102115639.png)

---

![image-20230302201440370](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102115722.png)

---

![image-20230306100923887](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102115075.png)

过拟合：理论上可以分成每一个叶子节点，不希望真的分类成一个个的个体

避免过拟合：剪枝操作

限制深度：假设深度到4，就不继续往下分了

限制叶子节点个数：叶子节点数小于4就不再细分

![image-20230306101243591](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102115208.png)

 后剪枝效果好，但是时间复杂度很大

---

### 2.3 CART

![image-20230306101654177](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102115817.png)

![image-20230306102246760](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102115149.png)

---

**分类树**

![image-20230306102603732](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102115985.png)

---

**回归树**

![image-20230306102705947](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102115476.png)



## 3. 支持向量机（SVM）

![image-20230306103658938](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102116925.png)

找到更好的分类方案

Large Margin 更好，因为更宽

---

![image-20230306103823257](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102116107.png)

---

![image-20230306104436178](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102116027.png)

---

![image-20230306104527185](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102116954.png)

---

![image-20230306104835265](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102116824.png)

---

![image-20230306105122599](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102116513.png)

![image-20230306105319879](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102116418.png)

![image-20230306105532739](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102116215.png)

---

![image-20230306105636120](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102116958.png)

软间隔：允许少量的样本不在自己的这个类别，分类并不严格，还是期望追求最大的壁

---

![image-20230306110307334](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102116571.png)

![image-20230306110400405](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102116596.png)

四维空间不好做可视化，之后降维到三维是不合理的，只是为了可视化方便



## 4. 神经网络

### 4.1 线性模型

![image-20230306143954759](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102116092.png)

---

### 4.2 分类与回归

![image-20230306144250944](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102116662.png)

![image-20230306144413056](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102116496.png)

![image-20230306144454161](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102116361.png)

---

### 4.3 感知机模型

![image-20230306144821722](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102116281.png)

![image-20230306145031184](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102116090.png)

隐藏层可以有很多层，每层都是一个f

Deep Learning = Neural Network

---

![image-20230306145451079](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102116028.png)

---

![image-20230306145833072](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102116830.png)

learning rate 太小移不动，learning rate 太大会形成梯度的振荡（爆炸）

---

![image-20230306151107876](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102117645.png)

批量大小一般为2的次幂

---

![image-20230306151647059](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102117950.png)

---

![image-20230306151756285](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102117017.png)

---

![image-20230306151854291](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102117680.png)

---

![image-20230306152441891](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102117713.png)

---

![image-20230306152451747](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102117503.png)

---

![image-20230306152705835](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102117408.png)

![image-20230306152922731](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102117682.png)

![image-20230306153440643](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102117511.png)

---

![image-20230306154510066](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102117143.png)

![image-20230306155702536](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102117248.png)

---

### 4.4 激活函数

![image-20230306160511551](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102117558.png)

![image-20230306161010332](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102117417.png)

Relu是当前学界和工业界最好用的激活函数之一

---

### 4.5 维度诅咒

![image-20230306161753533](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102117428.png)

![image-20230306161937237](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102117166.png)

![image-20230306162026439](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102117688.png)

![image-20230306162534170](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102118578.png)

---

### 4.6 过拟合与欠拟合

![image-20230307193415765](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102118057.png)

![image-20230307193828538](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102118285.png)

泛化误差：在验证集（测试集）上的准确度

过拟合：训练误差特别小，泛化误差特别大

欠拟合：训练误差和泛化误差都很大

---

![image-20230307194222038](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102118290.png)

正则化：限制模型的参数，进而限制模型的大小

数据增强：对数据集进行处理

降维：从模型的角度出发

集成学习：多个模型集成在一起

---

![image-20230307194419933](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102118417.png)

---

### 4.7 正则

![image-20230307194505732](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102118129.png)

---

**权重衰减：**

![image-20230307194620335](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102118093.png)

θ用来限制权重大小，θ是超参数，可以自己设定，用来约束权重的取值范围，防止过拟合的现象

柔性限制，(λ/2)||w||^2 可以看作是对权重项的惩罚

λ控制了正则项的重要程度

上图中的柔性限制是 L2正则

---

![image-20230307195001639](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102118810.png)

方差决定离散程度，方差越大，结果越分散；方差越小，结果越集中

偏差决定准确程度，偏差越大，结果越不准；偏差越小，结果越准确

---

两种正则方法——L1正则 和 L2正则

![image-20230310165503091](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102118716.png)

L1正则会使某些参数（比较小的参数）变成0，也就是会靠近某些轴 

L2正则会使整体的参数值变小，也就是会靠近原点 

---

**防止过拟合的手段：**

1. **Dropout**

   ![image-20230310170333656](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102118242.png)

   - Dropout

     Dropout是对节点进行随机失活，即赋0，与上述L1正则的赋0策略不同

     经过Dropout之后整个模型变得简单了

     训练的时候会随机选择一些节点进行失活，但是预测的时候全部节点都会参与

     Dropout在训练时随即砍掉一部分神经元让模型变简单，防止模型太复杂导致过拟合。而在测试的时候采用所有的神经元进行测试

     每轮Dropout都是对整个模型进行Dropout，每轮失活的节点都不太一样，Dropout之后的模型相当于原模型的子模型，每次Dropout都相当于是在训练一个子模型，但是最后会拿全部的节点进行预测，相当于拿之前训练好的一堆子模型进行一个预测，类似集成学习

   - 集成学习

     集成学习是在针对一个问题设计模型的时候，会设计多个模型，对这些模型进行统一的训练。将来解决问题的时候将这些模型都拿出来一起进行决策

2. **Early stopping** & **Data augmentation**

   ![image-20230310172003577](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102118727.png)

   早停法 和 数据增强

   - 早停法 Early stopping

     迭代次数越多，就会出现过拟合现象，所以可以早停

     当验证集上的错误率出现上升的时候，说明模型开始出现过拟合了，这时直接停掉就好了

     早停法就是监控验证集和训练集的错误率，选择一个停止训练的时间

   - 数据增强 Data augmentation

     对数据集进行一些操作（比如对图片进行随机旋转，原图就会通过变换得到一堆副本，把这些图片一起送回到数据集中，就可以增加数据集的容量），数据集变复杂，可以防止过拟合现象

     ![image-20230310172709592](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102118557.png)

---

![image-20230310172756620](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102119069.png)

---

### 4.8 数值稳定性

![image-20230310172957607](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102119549.png)

神经网络算法本质上就是加权连乘操作

连乘操作会导致梯度爆炸和梯度消失

---

**数据归一化处理**

![image-20230310185512464](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102119347.png)

- 归一化

  将数据映射到[0, 1]区间

- Z-Score标准化

  将数据映射到[-1, 1]区间

![image-20230310185902595](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102119846.png)

---

### 4.9 神经网络大家庭

#### 4.9.1 CNN——卷积神经网络

![image-20230310190355344](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102119748.png)

卷积神经网络使解决图像数据的变体算法

![image-20230310190529155](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102119541.png)

CNN对图片的处理是局部处理

---

#### 4.9.2 RNN——循环神经网络

![image-20230310191138411](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102119078.png)

应用在文本领域，是基于时序关系的

- t = 0 ---> 我
- t = 1 ---> 吃
- t =2 ---> 饭

RNN可以通过上图中的橙色连线，将之前处理过的信息传递下去

---

#### 4.9.3 GNN——图神经网络

![image-20230310191615153](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102119412.png)

推荐系统（用户画像）

![](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102119963.png)

- 节点 表征某种特征
- 边 表征特征和特征之间的关系
- 整体 表征图的性质

上述都可以通过向量表示 ---> 针对 节点、边、整体各自设计一个神经网络，分别将节点、边和整体的信息用向量送进神经网络里做学习做映射，得到更新之后的信息

```
例子：
	小猫小狗分类问题
	节点表示为猫狗的特征：猫眼睛、猫耳朵、...
	边表示特征之间的联系：眼睛和耳朵之间的联系是五官，可以抽象为一个向量
			猫尾巴和眼睛之间的联系联系不大，所以【抽象得到的向量的数值】比【眼睛和耳朵联系的向量】小
    整体表示某个整体的类别：一组向量表示猫这个类别，另一组向量表示狗这个类别...
    					总体就是一个整体信息
    上述都是超参数，自己定义用多少维的数据表示节点、边、整体
```

---

#### 4.9.4 GAN——生成对抗网络

![image-20230310192839977](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102119653.png)

![image-20230310193647172](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102119523.png)

- Generator：生成器

  通过生成器生成一张图片

  **生成器的目的是尽可能的生成一张很真实的图片，企图去骗过判别器**

- Discriminator：判别器

  将生成的图片送到判别器

  Real Samples：真实数据集，采集于真实世界中

  从生成的数据集和真实的数据集里随机进行抽样送进判别器里进行判别

  判别器的作用就是用来分辨当前送进来的数据是来源于真实数据的还是生成器生成的结果的（有监督训练）

  送进判别器的数据既有数据悠悠标签（比如0为生成器生成的，1为真实世界中的）

  判别完之后会把判别情况反馈回判别器

  **判别器的目的是尽可能的去分辨，分辨图片是来源于真实世界还是生成的图片**

当某一天，判别器判别不出生成器生成的图片是否来源于真实世界的时候，就说明生成器已经被训练到一个非常逼真的效果。对抗的关系，两者可以共同进化。



## 5. 迁移学习

迁移学习应用于数据集比较小，但是还想用DL的情况

迁移学习：把某些东西，从别的地方迁移过来，可以迁移实例、特征、模型、思想

---

![image-20230310201552195](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102119740.png)

---

![image-20230310200730159](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102119552.png)

> **例子**
>
> 之前的分类任务是识别猫和狗的，当前的任务是识别豹子和老虎的
>
> 之前识别猫和狗的特征，与豹子和老虎的特征是有一些类似的，完全可以把特征提取的部分原封不动的迁移过来，后边加入一个新的分类器（SVM、神经网络），重点是训练分类器。

---

![image-20230310201351461](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102119237.png)

---

![image-20230310201449334](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102119268.png)

（迁移思想）



# 三、无监督学习

## 1. 无监督算法——降维

### 1.1 降维概述

![image-20230311093104804](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303110931895.png)

![image-20230311093208931](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303110932985.png)

![image-20230311093322390](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303110933475.png)

![image-20230311093425056](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303110934101.png)

---

### 1.2 奇异值分解SVD

![image-20230311093533987](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303110935048.png)

奇异值分解就是把矩阵分解成三个矩阵的乘积

矩阵 ---> 正交矩阵U * 对角矩阵$\Sigma $ *正交矩阵V

![image-20230317142047285](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303171421595.png)

![image-20230317093452565](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303171421212.png)

对角矩阵起到拉伸的作用，正交矩阵起到旋转的作用

线性变换 = 旋转 + 拉伸 + 旋转

![image-20230311093628611](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303110936672.png)

U是左奇异向量。V是右奇异向量

![image-20230317142433604](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303171424675.png)

![image-20230317142242680](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303171422745.png)

![image-20230317170546593](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303171705652.png)

![image-20230317170722048](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303171707103.png)

---

#### 1.2.1 SVD计算案例

![image-20230317170814121](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303171708179.png)

![image-20230317170855624](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303171708687.png)

`疑问`：$\lambda$结果是负数的情况？

- 奇异值减小特别快——有主要特征和次要特征，奇异值越大，表征这个特征越重要
- 还可以做一些降维操作：$\begin{bmatrix}
    &107  &  &  &  &  & \\
    &  &21  &  &  &  & \\
    &  &  &6  &  &  & \\
    &  &  &  &0.5  &  &\\
    &  &  &  &  &0.02  &\\
    &  &  &  &  &  &0.01\\
  \end{bmatrix}$就会降维成$\begin{bmatrix}
    &107  &  &\\
    &  &21  &\\
    &  &  &6\\
  \end{bmatrix}$

![image-20230317171654070](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303171716121.png)

---

#### 1.2.2 一些应用

##### 1. 存储图像

![image-20230317171821992](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303171718046.png)

M = U $\cdot $ $\Sigma$ $\cdot$ $V^{T}$ 存储数据的时候，可以只存储这三个小矩阵，没必要存储M这个大矩阵

##### 2. 去噪

![image-20230317172310412](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303171723479.png)

M = U $\cdot $ $\Sigma$ $\cdot$ $V^{T}$ ，$\Sigma$ 的前几个奇异值都比较大，后几个都比较小，提取主要特征，重建回原本的像素空间，就会去掉一些噪声（去噪）

##### 3. 降维

![image-20230317172551431](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303171725540.png)

---



### 1.3 主成分分析（PCA）

![image-20230317173037713](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303171730779.png)

- 把数据映射到 F1轴上会更好点
- 降维要保证丢失的信息越少越好
- 主成分分析就是要找到F1
- F1叫做`第一主成分`
- 和F1垂直的F2叫做`第二主成分`

![image-20230320153241939](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303201532008.png)

1. 先找到数据的中心点
2. 在中心点做坐标轴，对这个坐标轴进行旋转
3. 看转到哪里的效果是最好的（分的最开，丢失的信息最少）（映射到坐标轴之后，方差最大，分布最分散）

![image-20230320153455019](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303201534094.png)

（均值归一化见【数学基础-统计学】）

![image-20230320153700946](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303201537011.png)

`协方差`表征的也是数据的离散程度（取值范围：-1 ~ 1）

协方差本身不可能超出（-1 ~ 1），除非对数据做了一些映射

![image-20230320154054730](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303201540799.png)

拉伸时只有对角线的值在变，因为他们的相关性没变，只是离散程度变了，即方差变了

旋转的时候，四个值都在变；逆时针旋转时，会慢慢变成正相关；顺时针旋转时，会慢慢变成负相关

---

PCA的算法两种实现方法：

1. 基于 SVD分解协方差矩阵 实现PCA算法

   ![image-20230320160514742](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303201605815.png)

2. 基于 特征值分解协方差矩阵 实现PCA算法

   ![image-202303201606047](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303201606047.png)

---

![image-20230320162752373](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303201627439.png)

![image-20230320162836157](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303201628207.png)

![image-20230320162934270](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303201629334.png)

---

PCA的缺点：

![image-20230320163009599](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303201630662.png)

---



### 1.4 t-分布领域嵌入算法【没懂】

t-SNE（t-distributed stochastic neighbor embedding）

![image-20230320163742353](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303201637402.png)

![image-20230320164016148](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303201640199.png)

把他映射到某个轴上，分类效果不是很好

---

t-SNE步骤：

![image-20230320164700765](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303201647826.png)

![image-20230320164717101](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303201647162.png)

![image-20230320164835198](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303201648254.png)

![image-20230320165113339](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303201651386.png)

先对数据做归一化，让数据处在同一个分布下，这样才能用统一是t-分布衡量它

![image-20230320165316515](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303201653559.png)

![image-20230320165359996](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303201654052.png)

相似度矩阵

![image-20230320165419564](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303201654615.png)

![image-20230320165445479](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303201654558.png)

把一个东西变成另一个东西：

1. 定义一个损失loss
2. 优化这个损失（梯度下降）

---



### 1.5 常见的降维算法

![image-20230320170047735](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303201700813.png)

[特征提取/数据降维:PCA、LDA、MDS、LLE、TSNE等降维算法的python实现](https://github.com/heucoder/dimensionality_reduction_alo_codes)

---



## 2. 无监督学习——聚类

![image-20230322085302042](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220853092.png)

![image-20230322102605191](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221026240.png)

### 2.1 K均值聚类

![image-20230322085655918](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220856978.png)

1. k值是超参数，自己设定；设置k为几，最后就会分成k类
2. 收敛的现象是均值不再发生变化

---

#### 2.1.1 示例

![image-20230322085851437](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220858500.png)

![image-20230322090013453](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220900513.png)

---

#### 2.1.2 距离的计算

![image-20230322090231414](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220902477.png)

距离分为`距离度量`和`非距离度量`

- 距离度量：满足上述四个性质
- 非距离度量：人、人马、马的相似性。非距离度量是主观打分

![image-20230322092841556](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220928604.png)

（常见距离小结）

##### 1. 曼哈顿距离（Manhattan Distance）

$$
dist_{man}(x_i, x_j) = ||x_i - x_j|| = \sum_{u=1}^{n}|x_{iu}-x_{ju}|
$$

![image-20230322091027530](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220910605.png)

- 红线相加就是曼哈顿据距离
- 可以应用在城市送外卖的距离计算
  - 假设蓝线就是送外卖的路线
  - 红线的长度和蓝线的长度相等

##### 2. 欧式距离（Euclidean Distance）

$$
dist_{ed}(x_i,x_j) = ||x_i-x_j||_{2} = \sqrt{\sum_{u=1}^{n}|x_{iu} - x_{ju}|^2}
$$

![image-20230322091529391](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220915433.png)

- 就是两点间的直线距离

##### 3. 切比雪夫距离（Chebyshev Distance）

![image-20230322091806982](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220918066.png)

- 沿着一个轴的最大距离，通常被称为期盼距离

##### 4. 闵氏距离（Minkowski）

![image-20230322092147554](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220921613.png)

##### 5. 余弦相似度（Cosine Similarity）

![image-20230322092309349](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220923417.png)

- 衡量角度
- 可以忽略幅度

##### 6. 汉明距离（Hamming Distance）

![image-20230322092657100](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220926160.png)

- 不是很常用

---

### 2.2 密度聚类

#### 2.2.1 DBSCAN（Density-based Spatial Clustering of Applications with Noise）

![image-20230322092939356](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220929411.png)

- 针对不同的数据分布，要选择不同的聚类方法

![image-20230322093211244](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220932298.png)

- $\varepsilon$是超参数
- 以这个$\varepsilon$为半径画的圆，这个范围就称为领域

![image-20230322093405395](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220934440.png)

- MinPts，最小样本点数量，也是超参数
- 在某个样本点的领域中，至少存在MinPts个样本点，则该样本点为一个核心对象

![image-20230322093943591](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220939643.png)

---

#### 2.2.2 示例

![image-20230322094126212](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220941273.png)

![image-20230322094351675](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220943733.png)

---

### 2.3 层次聚类

#### 2.3.1 Hierarchical Clustering

![image-20230322094741568](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220947669.png)

![image-20230322094950731](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220949791.png)

- 对距离不同的衡量标准，会形成不同的聚类效果

---

#### 2.3.2 示例

![image-20230322095206003](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220952060.png)

- 在哪里停，就是我们进行层次聚类的超参数

---

#### 2.3.3 层次聚类方法

![image-20230322095347491](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220953543.png)

---

#### 2.3.4 应用场景（生物信息学）

![image-20230322095503826](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220955889.png)

---

### 2.4 高斯混合模型聚类【注】

![image-20230322095737043](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303220957104.png)

- 上图是班级成绩的一个分布（化学成绩和地理成绩）
- 2016和2017的数据集不小心混在一起了，想要分开
- 适用于均值很像，重复的数据

#### 2.4.1 多项式拟合

![image-20230322100010367](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221000414.png)

- 把基底[1, $x$, $x^2$, $x^3$, ..., $x^n$]从幂次变成一个高斯函数 $g(x) = \frac{1}{\sqrt{2\pi}\sigma}e^{\frac{(x-\mu)^2}{2\sigma^2}}$

![image-20230322100605392](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221006453.png)

#### 2.4.2 高斯函数

![image-20230322100713017](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221007069.png)

![image-20230322100825313](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221008357.png)

#### 2.4.3 高斯混合模型

![image-20230322100843136](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221008176.png)

---

#### 2.4.4 高斯混合模型的训练过程

![image-20230322100953632](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221009687.png)

![image-20230322101026561](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221010609.png)

![image-20230322101211881](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221012925.png)

![image-20230322101252209](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221012254.png)

---

#### 2.4.5 得到三个参数【可以忽略】

![image-20230322101349713](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221013760.png)

![image-20230322101616623](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221016665.png)

![image-20230322101745108](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221017160.png)

![image-20230322101832264](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221018310.png)

![image-20230322101848992](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221018032.png)

极大似然：所见即所得，假设我们抽到的就是可能性最大的样本

![image-20230322102312275](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221023318.png)

---

![image-20230322102438629](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221024690.png)

---

### 2.5 性能度量

![image-20230322102955034](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221029066.png)

![image-20230322104337229](C:/Users/Administrator/AppData/Roaming/Typora/typora-user-images/image-20230322104337229.png)

#### 2.5.1 外部指标

![image-20230322103507346](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221035382.png)

![image-20230322103518014](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221035045.png)

#### 2.5.2 示例——外部指标

![image-20230322103110080](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221031127.png)

- $c_1$,$c_2$是聚类结果，$c_1^*$，$c_2^*$是真实情况
- a，b，c，d是四个类别
- JC、FMI、RI是衡量聚类效果的指标

#### 2.5.3 内部指标

![image-20230322103558137](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221035191.png)

1. DB指数

   ![image-20230322103914406](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221039451.png)

   - DBI越小越好，表明簇间分散，簇内紧密

2. Dunn指数

   ![image-20230322104157459](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221041511.png)

   - DI越大越好

#### 2.5.4 示例——内部指标

![image-20230322103633215](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221036258.png)

- 聚类结果：分成三类
- C是类别
- avg(C)是求这个簇的离散程度
- diam(C)是求每个类里边最大值的求解

![image-20230322103811991](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221038040.png)

---



# 四、强化学习

## 4.1 强化学习

### 4.1.1 Terminology

![image-20230323161833280](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231618351.png)

- state——状态
- action——代理的动作
- Environment——环境
- agent——代理

![image-20230323162056658](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231620719.png)

- policy——策略
- 概率密度函数：$\pi(a|s) = P(A = a | S = s)，s是状态state，a是动作action$。表示在s状态下执行a这个动作的概率

![image-20230323162602399](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231626466.png)

- Reward——agent从环境中接收的数值，作为对agent操作对未来局势影响的评判
  - 积极奖励——collection a coin，win the game
  - 消极奖励——touch a Goomba
  - 零奖励——nothing happens
- 奖励的规则是人定义的，定义的好坏可以直接影响结果

![image-20230323162922654](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231629719.png)

- state transition——状态转移函数

![image-20230323163120641](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231631696.png)

![image-20230323163133739](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231631800.png)

- Trajectory——轨迹
- 接受一个状态，做一个动作，得到一个奖励；继续接受一个新状态，做一个新动作，得到新奖励，如此反复，得到轨迹

![image-20230323163350641](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231633701.png)

- Return：回报（累计）
- 上图中的$R_t$是t时刻的Reward
- 未来的奖励没有当前的奖励重要
- $\gamma $ ——折扣率discount rate，是个0到1的数
- $U_t$——折扣回报，他只是一个随机变量。它依赖于未来所有的action和state

![image-20230323164003884](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231640935.png)

- 期望：对未来长期价值的衡量
- $Q_\pi (s_t, a_t)$——Action-Value Function，动作价值函数。是对 $U_t$ 的期望。`是对动作的衡量`。当前状态下，我做某个动作的期望。

![image-20230323165312853](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231653909.png)

- 状态价值函数
- $Q^*(s_t, a_t)$——Optimal action-value function，最优动作价值函数，是最优策略
- $V_\pi (s_t)$——State-value function，状态价值函数，`是对当前局势的衡量`。当前状态优势，该值就大，反之就小。
- $V_\pi (s_t)$ 是针对 $\pi$ 求的期望，$\pi(a|s_t)$ 是策略函数，是一个随机变量。$Q_\pi (s_t, a)$ 是对 $\pi (a|s_t)$ 价值的衡量
- 当Action是离散型时，$V_\pi (s_t) = \sum_{a} \pi (a|s_t) \cdot Q_\pi (s_t, a)$ 
- 当Action时连续型时，$V_\pi (s_t) = \int \pi (a|s_t) \cdot Q_\pi (s_t, a) da$ 

---

#### 价值函数的总结

![image-20230323170843775](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231708825.png)

![image-20230323171518278](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231715332.png)

#### 示例？

![image-20230323170956846](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231709898.png)

![image-20230323171100992](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231711050.png)

---

![image-20230323185645047](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231856105.png)

---



## 4.2 Value-based Learning

基于价值的学习

### 4.2.1 DQN(Deep Q Network)

![image-20230323185819226](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231858280.png)

![image-20230323190054441](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231900490.png)

- $w_t$是神经网络的参数
- $s_t$是神经网络接受的参数

![image-20230323190347795](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231903844.png)

- $s_{t+1} \sim p(\cdot|s_t, a_t)$ 是状态转移函数。他在不同的任务里是不一样的
- reward 和 label 的区别：
  - label 是数据的真值
  - reward 是对动作好坏的评定，是一个规则，需要自己定

---

![image-20230323190944802](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231909842.png)

- 需要把整段路程行驶完才可以更新一遍模型

![image-20230323191122559](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231911608.png)

- 并没有跑完全程，模型的预测时间是120min
- 跑完30min，继续让模型预测一下，预测时间是110min
- 110min 比120min 更可信，因为其中包含了一些真值，这就是TD的思想

![image-20230323192132624](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231921662.png)

![image-20230323192405312](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231924350.png)

![image-20230323192501696](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231925731.png)

---

### 4.2.2 DQN总结

![image-20230323192646720](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231926764.png)

![image-20230323192725080](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231927128.png)

---



## 4.3 State-based Learning

基于状态的学习

![image-20230323193158286](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303231931329.png)

59:5











































