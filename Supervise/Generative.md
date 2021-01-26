以二分类为例，  
数据空间上有两个类别的点，每个类别有一堆点。每个类别的点符合各自的分布。  
对于任意一个新的点，可以分别算出点属于两个分布的概率：$P(data|A)$和$P(data|B)$  
新的点属于概率较大的那一类，具体公式为：  

$$
P(class | data) = \frac{P(data|class)P(class)}{\sum_{class}P(data|class)P(class)}
$$