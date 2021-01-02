通过一些方法分析ML problem，选择最promising的方向去尝试。  

# 在训练集上表现好

增大网络容量  
Adam等优化算法

# 验证集上表现好

正则化  
增大训练集  

# 测试集上表现好

增大验证集

# 真实场景中表现好

更改验证集  
更改cost function

# other tips

1. 训练过程中不建议使用early stopping，因为它会同时使第一步变差第二步变好，不符合前面说的正交化。  
2. using a single number evaluation metric，如果有多个衡量指标，则  
（1）把指标分成optimizing metric和satisfying metric两类。前一种越。。。越好，后一种只要足够。。。就好。   
（2）如果有多个optimizing metric，则把它们合并成一个，例如F1 score。  