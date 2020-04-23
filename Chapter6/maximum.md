# 最大熵模型

## 模型

求公式（1）对数似然函数的极大值$$\hat w$$，再把$$\hat w$$代入公式（2）最大熵模型求出$$P_w(y|x)$$  

对数似然函数  
$$
\begin{aligned}
L(w) = \sum_{x,y} \tilde P(x, y) \sum_{i=1}^n w_if_i(x, y) - \sum_x \tilde P(x) \log Z_w(x)   && (1)
\end{aligned}
$$


最大熵模型：  
$$
\begin{aligned}
P_w(y|x) = \frac{1}{Z_w(x)}\exp (\sum_{i=1}^nw_if_x(x, y))   \\
Z_w(x) = \sum_y \exp (\sum_{i=1}^nw_if_x(x, y)) && {2}
\end{aligned}
$$

## 求公式（1）对数似然函数极大值的算法

改进的迭代尺度法（IIS） 