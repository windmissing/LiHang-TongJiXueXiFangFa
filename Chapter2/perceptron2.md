# 感知机 - 对偶形式

对偶形式的基本思想：  
将w和b表示为样本（书中术语为实例）$$x_i$$和标记$$y_i$$的线性组合形式，通过求解其系数而求得w和b  

但变形之后的感知机就从参数学习算法变成了非参数学习算法。因为它的算法模型中还要用到训练数据集X和y

## 模型

$$
\begin{aligned}
f(x) = sign(\sum_{j=1}^m a_jy_jx_j \cdot x + b)   \\
sign(x) = 
\begin{cases}
 +1, && x \ge 0 \\
 -1, && x \lt 0
 \end{cases}
\end{aligned}
$$
其中，m为样本数，n为样本的特征数

## 策略

感知机的损失函数是一个经验风险函数：  
$$
L(w, b) = - \sum_{x_i \in M}y_i (\sum_{j=1}^m a_jy_jx_j \cdot x_i + b)
$$
其中M是误分类点的集合

感知机的学习策略是从假设空间中选取使损失函数最小的模型参数a, b

## 算法

学习模型的具体方法  
感知机对偶形式使用随机梯度下降法  
$$
\begin{cases}
a_{new} = a_{old} + \eta \\
b_{new} = b_{old} + \eta y_i
\end{cases}
$$
