---
layout: post
title: Solve the Class-Imbalanced Problem
category: MacLearn
tags: machine-learning class-imbalanced
comments: true
---

In the imbalanced class distribution cases, the classifiers tend to produce high classification accuracies on the majority calss but poor classification accuracies on the minority ones. Class imbalance problem has been studied by many researchers, and the proposed methods can be categorized under three headings:

* **Pre-sampling methods**  
    makes the training set balanced, either by oversampling the minority class or by undersampling the majority class.
* **Cost-sensitive methods**  
    assigns a higher misclassification cost to the minority class than to the majority class. 
* **Other methods**  
    integrating sampling with training process.


![Pic](https://freemang.github.io/public/img/2017-08-21-class-imbalance.png)
A mindmap that summarizes the methods referred in [2].


*P.S*  
A python package offering a number of re-sampling techniques commonly used in datasets showing strong between-class imbalance [3]. [imbalanced-learn](http://contrib.scikit-learn.org/imbalanced-learn/stable/index.html)


*Reference*   
[1] Nitesh Chawla, Kevin Bowyer, Lawrence Hall, W Philip Kegelmeyer. (2002). **SMOTE: Synthetic Minority Over-sampling Technique.** [JMLR](http://dl.acm.org/citation.cfm?id=1622416)  
[2] Minlong Lin, Ke Tang, Xin Yao. (2013). **Dynamic Sampling Approach to Training Neural Networks for Multiclass Imbalance Classification.** [IEEE TNNLS](http://dx.doi.org/10.1109/TNNLS.2012.2228231)   
[3] [Imbalanced-Learn](http://contrib.scikit-learn.org/imbalanced-learn/stable/#) (A Python Toolbox to Tackle the Curse of Imbalanced Datasets in Machine Learning)