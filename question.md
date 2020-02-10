2. [梯度下降法的收敛证明](https://windmising.gitbook.io/lihang-tongjixuexifangfa/perceptron/4)  
公式（7），怎么证明$$\hat w_0 \cdot \hat w_{opt} \ge 0$$？

3. CS229里面说感知机算法没有数学依据？

4. [决策树的剪枝算法](https://windmising.gitbook.io/lihang-tongjixuexifangfa/decisiontree/5)  
只实际了递归算法，怎么用DP实现？

5. [CART树的剪枝](https://windmising.gitbook.io/lihang-tongjixuexifangfa/cart/7)  
为什么算法2步要强调自下而上计算g(t)？既然要把所有的a求出来，先算哪个结点的a应该不影响结果。    

6. [$$A(\delta|w)$$和$$B(\delta|w)$$推导]
$$A(\delta|w)$$的推导   
(https://windmising.gitbook.io/lihang-tongjixuexifangfa/option/10)  
公式（3）怎么推导到公式（4）  

7. [$$A(\delta|w)$$和$$B(\delta|w)$$推导]
(https://windmising.gitbook.io/lihang-tongjixuexifangfa/option/10)  
$$B(\delta|w)$$的推导 
**一次只优化其中一个变量$$\delta_i$$，而固定其它变量$$\delta_j,i \neq j$$**，得：  
【？】是一只优化一个$$w_i$$还是一个$$\delta_i$$？
【？】如果是只优化一个$$w_i$$，为什么不能直接假设其它$$\delta_j=0$$？  
【？】如果是只优化一个$$\delta_i$$，为什么算法6.1步骤2-(b)只更新一个$$w_i$$？

8. [拟牛顿法](https://windmising.gitbook.io/lihang-tongjixuexifangfa/option/11)
算法没看懂  

9. [线性可分SVM](https://windmising.gitbook.io/lihang-tongjixuexifangfa/2)  
7.1.3存在性和w的唯一性没看懂

10. [原始问题转换为对偶最优化问题](https://windmising.gitbook.io/lihang-tongjixuexifangfa/7/8)  
公式（5）代入公式（3）怎么得到公式（6）

11. [训练误差分析](https://windmising.gitbook.io/lihang-tongjixuexifangfa/adaboost/2)  
公式（5）怎么得到公式（6）

12. [7.3.2 正定核](https://windmising.gitbook.io/lihang-tongjixuexifangfa/11/14)  
这一节从3开始就看不懂了，很多术语不懂  

13.
> 感知机学习算法的原始形式和对偶形式与第7章中支持向量机学习算法的原始形式和对偶形式相对应。  

感知机中的对偶与后面算法中的对偶是怎么对应的？

14. [用kd树的k近邻搜索](https://windmising.gitbook.io/lihang-tongjixuexifangfa/knn/3)  
这种搜索方法办能搜最近邻，算法求能搜出k近邻，怎么从最近邻得到k近邻？  