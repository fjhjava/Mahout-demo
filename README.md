# Mahout-demo
``` xml
Mahout 是一个很强大的数据挖掘工具，是一个分布式机器学习算法的集合，
包括：被称为Taste的分布式协同过滤的实现、分类、聚类等。
Mahout最大的优点就是基于hadoop实现，把很多以前运行于单机上的算法，转化为了MapReduce模式，
这样大大提升了算法可处理的数据量和处理性能。
```
### 推荐系统
 Mahout中和推荐系统相关内容有四个部分:
 -  Preference类: 表示每个用户或者物品的属性, 如{1: {2: 1.0, 3: 2.0}} 表示用户2和3分别对1进行了评价, 评分分别为1.0和2.0
 -  DataModel类: 表示所有的数据集合, 即Preference的聚合. DataModel可以是代码输入或者HTTP参数获取, 也可以从文件或者数据库中读取.
 
 - Similarity类: 表示所有Preference两者之间的相似度, 所有的用户或者物品都通过Similarty建立起了联系,
 所以这个是非常重要的, Similarity的选择和数据的类型有很大关系. Neighberhood记录每个用户或者物品相似的物品集, 方便后期调用.
 
-  Recommender类: 表示推荐算法, 整个系统的核心。 如何使用前面的Preference, DataModel, Similarity以及Neigherhood都将结合在Recommender来来使用。 
