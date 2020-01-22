# 朴素贝叶斯

分类算法、生成算法  
假设用于分类的特征在类确定的条件都是条件独立的。 

# 模型

$$
P(Y=C_k|X=x) = \frac {P(Y=C_k)\prod_jP(X^{(j)}=x^{(j)}|y=C_k)}{\sum_k P(Y=C_k)\prod_jP(X^{(j)}=x^{(j)}|y=C_k)}, k=1,2,\cdots,K
$$

# 策略

使后验概率最大化

# 算法