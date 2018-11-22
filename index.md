---
layout: cv
title: Fuxu Liu
pdf: true
---
# 刘福旭

<div id="webaddress">
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
- 期望职位：计算机视觉工程师/机器学习工程师
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

## 项目经历

### __基于Unet的盐矿图像分割__ `2018.9 - 2018.10`
_Programmer_<br>
此项目为kaggle的“TGS Salt Identification Challenge”比赛，比赛的任务是基于地震图像来判断是否具有盐矿，并对盐矿进行图像分割，获得更准确的盐矿位置，本人在比赛的最终排名为53/3234(top2%，银牌)。
Solution:
1. 基于Se-ResNext50为backbone的Unet。
2. 在Unet的Decoder部分加入SCSE block，并使用HyperColumn引入多尺度的图像，以获得具有更多信息的Feature。
3. 在模型中引入Deep Supervision机制，即在最后引入一个二分类模型（有盐/无盐），和multi-loss，更加有效地防止过拟合，和加快收敛速度。
4. Loss function使用最新发表的Lovasz loss，单独训练lovasz loss比bce+lovasz loss更能IOU精度。
5. 在模型训练的阶段中，使用了SGDR和cycle learning rate，以逃离局部最优点，而找到下一个更优的局部最优点。
<br>

### __基于目标检测的自动收银解决方案__  `2018.7 - 至今`
_Programmer_<br>
此项目旨在解决超市/零售商店或高校食堂，当较多人数排队结账时所造成的拥堵问题。本人在YOLO-V3的基础上，重新训练了基于商品/菜品数据的模型，目前获得较好的效果。目前在不同的模型中作对比，获取精度和是实时性更好的模型，并且尝试去优化模型。基于计算机的快速与高准确率的检测，可很大程度地减缓排队的拥堵问题，也提高了结账效率。
<br>
### __基于视觉的肺炎检测__ `2018.9 - 至今`
_Programmer_<br>
此项目为Kaggle的“RSNA Pneumonia Detection Challenge”比赛，本人目前将肺炎患者不透明的区域的x, y, width, height转换为mask，以供UNet模型进行训练，使用图像分割进行结果预测，目前在top6%名次，后期还会继续尝试去做改善。
<br>
### __基于内容的图像检索系统__ `2018.3 - 2018-5`
_Programmer_<br>
此项目旨在解决用户在寻找大量相似图片/或找寻类似的图片。本人在不同的预训练CNN模型上，尝试提取最后卷积层的feature map，将用户上传的图片也进行相同的卷积预处理而获得feature map，然后进行相似度量函数对比，而获得Top-K的相似图片，后返回到用户。
<br>
### __基于视觉的无人驾驶模拟玩家__ `2018.3 - 2018.5`
_Programmer_<br>
此项目旨在在GTA游戏的模拟真实驾驶环境下，进行大量的手动驾驶数据的收集，用于训练CNN模型，从而获得高精度的驾驶方向判断，可用于游戏中的模拟自动驾驶。

## 获奖荣誉

校二等奖学金 `2016` <br>
优秀大学生 `2016` <br>
校一等奖学金 `2017` <br>
优秀大学生 `2017` <br>
优秀学生干部 `2017` <br>

## 个人技能
- 编程语言：Python/C++
- 框架：TensorFlow/Keras/Sklearn/Python
- 图像处理：Opencv
- 算法：基础算法与数据结构/传统机器学习算法/DNN/CNN
- 数据库相关：MySQL
- 操作系统：Win/Linux

## 致谢
感谢您花时间阅读我的简历，期待能有机会和您共事。
<!-- ### Footer
-->
