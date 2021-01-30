以二分类为例，  
数据空间上有两个类别的点，每个类别有一堆点。每个类别的点符合各自的分布。  
对于任意一个新的点，可以分别算出点属于两个分布的概率：$P(data|A)$和$P(data|B)$  
新的点属于概率较大的那一类，具体公式为：  

$$
P(class | data) = \frac{P(data|class)P(class)}{\sum_{class}P(data|class)P(class)}
$$

其中:  

$$
P(class) = \frac{class\text{的样本数}}{\text{总的样本数}}
$$

$P(data|class)$与这个class的分布有关.  
重点是怎么根据某个class的已有样本推测class的[分布](https://windmissing.github.io/mathematics_basic_for_ML/Probability/distribution.html)  

# data是离散变量  

离散变量通常假设它符合Bernoulli 分布或者Multinoulli 分布,那么  

$$
P(data|class) = \frac{class\text{的样本数}}{\text{总样本数}}
$$

# data是连续变量

适用于连续变量的分布有很多,通常假设为高斯分布.  
1. 根据已有的训练数据求出$\mu$和$\sigma$, 高维数据时方差$\sigma$用协方差矩阵$\Sigma$代替.  

$$
\begin{aligned}
\mu = \frac{1}{N}\sum x^i \\
\Sigma = \frac{1}{N}\sum(x^i-\mu)(x^i-\mu)^\top
\end{aligned}
$$


2. 代入高斯分布的公式,就得到了整个class的分布.  

[高斯分布](https://windmissing.github.io/mathematics_basic_for_ML/Probability/distribution.html)  


# 其它

所以维度独立,朴素贝叶斯  
P27, posterior probability  
P15, Cross Entropy VS Square Error  
P16 Discriminative VS Generative  
