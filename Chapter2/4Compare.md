"对机器学习的性能进行比较"时存在的问题：  
1. 希望评估的是泛化性能，实际评估的是测试集性能  
2. 测试集性能与测试集的选择有关  
3. 算法本身具有随机性  
统计假设检验（hypothesis test）:  
- 如果：测试集上A比B好  
- 那么：A的泛化性能是否优于B？优于B的可能性有多大？  

# 2.4.1 假设检验

[显著度、置信度、自由度](https://www.zhihu.com/question/64441961)  

# 2.4.2 交叉验证t检验

模型A：$\epsilon_1^A, \epsilon_2^A, \cdots, \epsilon_k^A$  
模型B：$\epsilon_1^B, \epsilon_2^B, \cdots, \epsilon_k^B$  

假设检验的前提是：测试错误率为泛化错误率的独立采样   
交叉验证的局限：测试错误率并不独立，导致过高估计假设成立的概率  
解决方法：  
10折交叉验证 --> 5次2折交叉验证  
$\Delta_a^b$代表第a次第b折上的错误率  
[?] 为什么$\mu$只用第一次的？  
[?] 最后一句没看懂。公式2.32没看懂  

# 2.4.3 McNemar检验

列联表 contingency table  
[?] 连续性校正

[卡方分布](https://windmissing.github.io/mathematics_basic_for_ML/Probability/distribution.html)  

# 2.4.4 Friedman检验与Nememyi后续检验

使用场景：在一组数据集上对多个算法进行比较  
一个数据集 -> 一组数据集  
两个算法 -> 多个算法  

后面没继续看了