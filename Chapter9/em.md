EM算法是一种迭代算法，用于含有隐变量(hidden variable)的概率模型的极大似然估计，或极大后验概率估计。

E：expectation，求期望   
M：maximization，求极大  
E、M代表了EM算法中最重要的两个步骤  

# 模型

含有隐变量的概率模型  
EM算法可用于生成模型的非监督学习。  
生成模型由联合概率分布P(X,Y)表示，可以认为非监督学习训练数据是联合概率分布产生的数据。  
X为观测数据，Y为未观测数据。  

# 策略

极大化观测数据（不完全数据）Y关于参数$$\theta$$的对数似然函数，即极大化：  
$$
\begin{aligned}
L(\theta) = \log P(Y|\theta) = \log\sum_zP(Y,Z|\theta) \\
= \log(\sum_Z P(Y|Z, \theta)P(Z|\theta))
\end{aligned}
$$

# 算法

