---
layout: post
title: 机器学习分类算法的评价
category: MacLearn
tags: machine-learning
comments: true
---

### 二分类问题混淆矩阵

![confusion matrix](http://freemang.github.io/public/img/2017-07-12-evalutation-of-classification.png)

### 正/负  

|index     |equation     |
|:---------|:-----------:|  
| 预测正例 | P = TP + FP |   
| 预测负例 | N = FN + TN |  
| 实际正例 | FP + FN     |  
| 实际负例 | FP + TN     |  
| 正确率   | accuracy = (TP + TN) / (P + N) |  
| 错误率   | error rate = (FP + FN) / (P + N) = 1 - accuracy |  

### 灵敏度/特异性/精度/召回率

|index     |equation     |description     |
|:---------|:-----------:|:---------------|  
| 灵敏度 + | sensitive = TP / (TP + FN)   | 表示 **实际正样本** 中 **预测正样本** 的比例 |
| 特异性 - | specificity = TN / (FP+TN)   | 表示 **实际负样本** 中 **预测负样本** 的比例 |
| 精度     | precision= TP / (TP + FP)    | 表示 **预测正样本** 中 **实际正样本** 的比例 |
| 召回率   | recall=TP / (TP + FN) = sensitive | 表示 **实际正样本** 中 **预测正样本** 的比例 |

### ROC axis

|axis      |index        |equation  |description |
|:---------|:------------|:--------:|:---------- |
|x-axis|False positive rate| FPR = FP / (FP + TN) = 1 - specificity| **实际负样本** 中被 **错误预测为正样本** 的概率|
|y-axis|Truth positive rate| TPR = TP / (TP + FN) = sensitivity    | **实际正样本** 中被 **正确预测为正样本**的概率|


*P.S.*  
通常分类器的输出为0~1的概率值(score)，预测的结果是根据设定的阈值(thre)而定。比如thre=0.5, 则score>0.5为正样本，score<0.5为负样本。通过设定不同的阈值，得到多个ROC空间的值，将这些值绘制成ROC空间的曲线，即为ROC曲线。
