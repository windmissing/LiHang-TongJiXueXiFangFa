# 序列最小最优化算法

SMO，sequential minimal optimization

## SMO的使用场景

SMO用于解决非线性支持向量机的对偶问题：  
$$
\min_a \quad \sum_{i=1}^N\sum_{j=1}^Na_ia_jy_iy_jK(x_i, x_j) - \sum_{i=1}^Na_i  \\
s.t. \quad \sum_{i=1}^Na_iy_i=0
\quad \quad 0 \le a_i \le C, i=1,2,\cdots,N   \tag {1}
$$

## SMO的原理

如果所有变量$$a_i$$都满足此问题的KKT条件。  
否则，选两个变量，固定其他变量，针对这两个变量构建一个二次规划问题。   
由于这两个变量是互相制约的，可以用一个变量来表示另一个变量，因此只有一个自变量。  
解二次规划问题并更新变量。  

## SMO的过程

1. 选择两个变量[link](https://windmising.gitbook.io/lihang-tongjixuexifangfa/smo/16)，假设两个变量为$$a_1$$和$$a_2$$  
2. 把公式（1）中的变量$$a_1$$、$$a_2$$和常量分开来写[link](https://windmising.gitbook.io/lihang-tongjixuexifangfa/smo/17)，成为公式（2）  
$$
L(a_1, a_2) = f(1,1)+2f(1,2)+f(2,2) \\
+2\sum_{j=3}^Nf(1,j) +2\sum_{j=3}^Nf(2,j) \\
-a_1 - a_2 + 常数项\tag {2}
其中：
f(i, j) = a_ia_jy_iy_jK(x_i,x_j)
$$
3. 根据$$a_1$$和$$a_2$$的关系，消息公式（2）中的变量$$a_1$$，留下变量$$a_2$$，得到公式（3）[link](https://windmising.gitbook.io/lihang-tongjixuexifangfa/smo/18)  
4. 公式（3）对$$a_2$$求导，并令导数为0，得到$$a_2$$的值[link](https://windmising.gitbook.io/lihang-tongjixuexifangfa/smo/19)。  
5. 第4步得到的$$a_2$$没有考虑到公式（1）的限制条件，需要对$$a_2$$做一些修剪[link](https://windmising.gitbook.io/lihang-tongjixuexifangfa/smo/20)  
6. 根据$$a_2$$得到$$a_1$$  
7. 根据新的$$a_1$$和$$a_2$$更新b  
8. 回到第1步