---
layout: post
title: Three Component of Learning Algorithms
category: MacLearn
tags: machine-learning 
comments: true
---

*A Few Useful Things to Know about Machine Learning*

### Learning = Representation + Evaluation + Optimization

* **Representation**  
A classifier must be represented in some formal language that the computer can handle. Conversely, choosing a representation for a learner is tantamount to choosing the set of classifiers that it can possibly learn. This set is called the hypothesis space of the learner. If a classifier is not in the hypothesis space, it cannot be learned. A related question, which we will address in a later section, is how to represent the input, i.e., what features to use.     
* **Evaluation**  
 An evaluation function (also called objective function or scoring function) is needed to distinguish good classifiers from bad ones. The evaluation function used internally by the algorithm may differ from the external one that we want the classifier to optimize, for ease of optimization (see below) and due to the issues discussed in the next section.  
* **Optimization**  
Finally, we need a method to search among the classifiers in the language for the highest-scoring one. The choice of optimization technique is key to the efficiency of the learner, and also helps determine the classifier produced if the evaluation function has more than one optimum. It is common for new learners to start out using off-the-shelf optimizers, which are later replaced by custom-designed ones.

![img](https://freemang.github.io/public/img/2017-08-04-three-component-of-learning.png)

---  

与之对应的，在《统计学习方法》的1.3节，也有对统计学习方法三要素的总结：
### 方法 = 模型(Model) + 策略(Strategy) + 算法(Algorithm)
* **模型**  
所要学习的条件概率分布或决策函数。
* **策略**  
模型选择的准则。
* **算法**  
实现求解最优模型的算法。

*Reference*   
[1] Pedro Domingos (2012). **A Few Useful Things to Know about Machine Learning.** [Communications of the ACM](https://doi.org/10.1145/2347736.2347755)  
[2] 李航 (2012). **《统计学习方法》** [清华大学出版社]()
