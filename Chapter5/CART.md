# CART决策树

CART：Classification And Regression Tree  
最小二乘回归树

## 回归树模型
$$
f(x) = \sum_{m=1}^{M}C_mI(x \in R_m)
$$

所设CART树分成了M个叶子结点，每个叶子结点对应的输出标签为$C_m$

即：
$$
f(x) = Cm, if x \in R_m
$$

## 划分

选择第j个特征$$x^{(j)}$$和它的取值s：  
$$
R_1(j, s) = \{x | x^{(j)} \le s\}  \\
R_2(j, s) = \{x | x^{(j)} \gt s\}
$$

## 策略

寻找最优变量j, s使得R1、R2的平方误差之和最小  

## CART和ID3、C4.5的区别

|ID3、C4.5|CART|
|---|---|
|基于feature划分|基于(feature, value)划分|
|该特征可以有几个取值，就划分成多少个子树|2叉树|
|该特征的每一个取值对应一个子树|分为X[:,feature]<=value和X[:,feature]>value|