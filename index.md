---
layout: cv
title: Fuxu Liu
pdf: true
---
# 刘福旭

<div id="webaddress">
<i class="fi-home" style="margin-left:1em"></i>
<a href="904849722@qq.com" style="margin-left:0.5em">904849722@qq.com</a>
<i class="fi-mail" style="margin-left:1em"></i>
<a href="liufx@dgut.edu.cn" style="margin-left:0.5em">liufx@dgut.edu.cn</a>
</div>

## 个人信息
- 刘福旭/男/1995
- 联系方式：15728134982
- 邮箱：904849722@qq.com
- 微信：m656120722
- csdn博客: [https://blog.csdn.net/Gary___](https://blog.csdn.net/Gary___)
- github: [https://github.com/Gary-Deeplearning](https://github.com/Gary-Deeplearning)
- 微信公众号：Gary_Cver
- 期望职位：计算机视觉工程师/深度学习工程师
- 期望城市：深圳/广州

## 教育经历

### __东莞理工学院__ `2015.9 - 至今`
```
Guangdong, Dongguan
```
- 网络工程
- GPA：3.52
- 主修课程：《算法与数据结构》、《高等数学》、《离散数学》、《面向对象编程》等
- 曾任职务：班长

## 工作经历

### 稀牛学院数据科学助教
_工作职责_<br>
- 负责对相关数据科学课程，如深度学习/数据分析等课程的学生答疑与作业批改。
- 间歇主讲某写相关主题内容，如竞赛经历与竞赛技巧。

## 项目经历

### __基于Unet的盐矿图像分割__ `2018.9 - 2018.10`
_Programmer_<br>
此项目为kaggle的“TGS Salt Identification Challenge”，比赛的任务是基于地震图像来判断是否具有盐矿，并对盐矿进行图像分割，获得更准确的盐矿位置，本人在比赛的最终排名为53/3234(top2%，银牌)。
_Solution_<br>
- 基于Se-ResNext50为backbone的Unet。
- 在Unet的Decoder部分加入SCSE block，并使用HyperColumn引入多尺度的图像，以获得具有更多信息的Feature。
- 在模型中引入Deep Supervision机制，即在最后引入一个二分类模型（有盐/无盐），和multi-loss，更加有效地防止过拟合，和加快收敛速度。
- Loss function使用最新发表的Lovasz loss，单独训练lovasz loss比bce+lovasz loss更能IOU精度。
- 在模型训练的阶段中，使用了SGDR和cycle learning rate，以逃离局部最优点，而找到下一个更优的局部最优点。
<br>

### __基于CNN的涂鸦识别__ `2018.9 - 至今`
_Programmer_<br>
此项目为Kaggle的“Doodle Recognition Challenge”，任务为建立模型以识别340个种类的涂鸦图画，目前排名top2%。<br>
_Solution_<br>
- 数据预处理，将数据中涂鸦的笔画利用Opencv绘成图片的格式，以作为CNN的Input。
- 分别将笔画以1/3分为A,B,C，在结合AB,AC,ABC，最后形成6-channels的Input，再将6-channels与Se-Resnext50结合，以增多模型提取的特征，也有效地提高了精度。
- 由于数据量较大，在训练的过程中，在256甚至更大的batch下，以较大的learning_rate训练，比小batch和小learning_rate，模型训练的更好。
- Stack，利用多个不同的模型，如ResNet50,se_Resnext50等，进行特征提取，将特征concatenate，再传入分类器。
- 在模型test阶段，利用confusion matrix，可以找到模型在哪个类别上容易预测错，手动设置threshold，以更好的适应相似类别的预测。
<br>

### __基于目标检测的自动收银解决方案__  `2018.7 - 至今`
_Programmer_<br>
此项目旨在解决超市/零售商店或高校食堂，当较多人数排队结账时所造成的拥堵问题。<br>
_Solution_<br>
- 以YOLO-V3为baseline，重新训练了基于商品/菜品数据的模型，且获得较好的效果。
- 尝试更换backbone，如ResNet50/101，可以获得比DarkNet53为backbone更好的准确率。
_TODO_<BR>
- 考虑到这个项目对准确率要求更高，适合的检测度即可，后期可考虑更好RetinaNet。
- 考虑到可能有不同的商品重叠的位置较大，为了防止NMS剔除掉正确的Box，加入Soft NMS使得有可能正确的box而保留了下来。
- 考虑到经过不断的卷积操作之后，小目标在高层网络的特征图会很小，丧失较多信息，因此加入HyperColumn，以保留下小目标的特征，对小目标的检测有一点的performance提高。
<br>
  
### __基于内容的图像检索系统__ `2018.3 - 2018-5`
_Programmer_<br>
此项目旨在解决用户在寻找大量相似图片/或找寻类似的图片。
_Solution_<br>
- 将图片数据不同的预训练CNN模型上，提取最后卷积层的4096维度的feature map，设定阈值为0.5，而获得0/1二值检索向量。
- 将用户上传的图片也进行相同的卷积预处理而获得feature map，然后进行相似度量函数（这里我仅用了L2距离来测试）对比，而获得Top-K的相似图片，后返回到用户。
_TODO_<br>
- 采用END-TO-END方法，loss function选用triplet loss或contrastive loss。
<br>

### __基于视觉的无人驾驶模拟玩家__ `2018.3 - 2018.5`
_Programmer_<br>
此项目旨在在GTA游戏的模拟真实驾驶环境下，训练一个可以自动驾驶的玩家。
_Solution_<br>
- 手动收集多个移动方向的图片驾驶数据，用于训练self=designed CNN模型。
- 使用预训练CNN，可以更好的提高准确率。
- 构造一个end-to-end模型，可同时进行检测和图像分类，在多任务分支的情况下，有效避免过拟合，在车/行人的目标检测下，保持设定的距离。

## 获奖荣誉
校二等奖学金 `2016` <br>
优秀大学生 `2016` <br>
校一等奖学金 `2017` <br>
优秀大学生 `2017` <br>
优秀学生干部 `2017` <br>
校二等奖学金 `2018` <br>
优秀大学生 `2018` <br>

## 个人技能
- 编程语言：Python/C++
- 框架：Pytorch/Keras/Sklearn/Python
- 图像处理：Opencv
- 算法：基础算法与数据结构/传统机器学习算法/DNN/CNN
- 数据库相关：MySQL
- 操作系统：Win/Linux

## 致谢
感谢您花时间阅读我的简历，期待能有机会与您共事。
<!-- ### Footer
-->
