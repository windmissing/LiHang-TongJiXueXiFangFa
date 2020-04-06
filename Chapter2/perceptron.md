# 感知机 perceptron

## 算法类型

二分类算法、线性分类模型、判别模型、监督学习算法

## 模型

模型是指所要学习的条件概率分布或者决策函数

$$
\begin{aligned}
f(x) = \text{sign}(w \cdot x + b)   \\
\text{sign} = 
\begin{cases}
 +1, && x \ge 0 \\
 -1, && x \lt 0
 \end{cases}
\end{aligned}
$$

## 策略

策略是指按照什么样的准则学习或者选择最优的模型。  
感知机的损失函数是一个经验风险函数：  
$$
L(w, b) = - \sum_{x_i \in M}y_i (w \cdot x_i + b)
$$
其中M是误分类点的集合

感知机的学习策略是从假设空间中选取使损失函数最小的模型参数w, b

## 算法

学习模型的具体方法  
感知机使用随机梯度下降法  
$$
\begin{cases}
w_{new} = w_{old} + \eta y_ix_i \\
b_{new} = b_{old} + \eta y_i
\end{cases}
$$

【？】CS229里面说感知机算法没有数学依据