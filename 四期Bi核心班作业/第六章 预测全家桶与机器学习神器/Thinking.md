[TOC]

# 第六章 预测全家桶与机器学习神器

---

## Thinking1  XGBoost与GBDT的区别是什么？      简要说明这两者之间的区别（10points） 

1. GBDT是机器学习算法，XGBoost是该算法的**工程实现**
2. 在使用CART作为基分类器时，XGBoost显示地加入了**正则项**来控制模型的复杂度，有利于防止过拟合，从而提高模型的泛化能力
3. GBDT在模型训练时，只是用了**代价函数的一阶导数**信息，XGBoost对代价函数进行二阶泰勒展开，可以同时使用一阶和**二阶导数**
4. 传统的GBDT采用CART作为基分类器，XGBoost支持**多种**类型的**基分类器**，比如线性分类器
5. 传统的GBDT在每轮迭代时使用**全部的数据**，XGBoost则采用了与随机森林相似的策略，支持对数据进行**采样**
6. 传统的GBDT没有设计对缺失值进行处理，XGBoost能够自动学习出**缺失值的处理策略**

## Thinking2  举一个你之前做过的预测例子（用的什么模型，解决什么问题，比如我用LR模型，对员工离职进行了预测，效果如何...  请分享到课程微信群中）  简要说明之前做过的例子，用的模型，解决的问题，并且在群里分享（10points）        

* 员工离职率预测：主要进行数据清洗、分析，使用的xgboost模型，5折交叉验证，得分0.81，后来借鉴了同学的方案，使用了LR模型，得分到0.84。后来做特征工程groupby，数据MaxMinscalar归一化，xgb和lr55分融合，效果都没有直接lr好。

## Thinking3  请你思考，在你的工作中，需要构建哪些特征（比如用户画像，item特征...），这些特征都包括哪些维度（鼓励分享到微信群中，进行交流）  能对工作场景，以及构造的特征进行洞察，在班级群中分享（10points）        

* 用户属性：基本属性，行为属性，统计属性

  * 行为属性包含时间维度、空间维度、周期维度

  * 统计属性包含简单统计量、复杂分析值

* 特征工程

  * 使用groupby构建类别与类别、类别与数值之间的特征，比如count、unique、min、max、sum、mean等

  * 将一个column分解为三个以增加特征维度

  * 将时间戳转化为time、day、hour
  * 对比column之间的值，构建unique特征（0，1）列
  * 相关特征进行交叉增加维度
  * 大小写的变化
  * 同一column相同意思的不同str转化为相同的str
  * 众数填充0值

---

---

---





Action1  男女声音识别     数据集：voice.csv     3168个录制的声音样本（来自男性和女性演讲者），采集的频率范围是0hz-280hz，已经对数据进行了预处理     一共有21个属性值，请判断该声音是男还是女？     使用Accuracy作为评价标准      1、完成代码（30points）     2、分享经验（30points）     3、得分Top3（10points）  




| 分类           | 内容                                                         | 数据集                                                       | 是否了解掌握 | 评阅点                                                       | GitHub代码 |
| -------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------ | ------------------------------------------------------------ | ---------- |
| 课上理解部分   |                                                              |                                                              |              |                                                              |            |
| 工具           | LR工具使用                                                   |                                                              |              |                                                              |            |
| 工具           | SVM工具使用                                                  |                                                              |              |                                                              |            |
| 原理           | FM模型：FM，FFM，DeepFM，NFM，AFM                            |                                                              |              |                                                              |            |
| 原理           | LR优点及缺点                                                 |                                                              |              |                                                              |            |
| 原理           | SVM优点及缺点                                                |                                                              |              |                                                              |            |
| 原理           | FM与LR区别                                                   |                                                              |              |                                                              |            |
| 原理           | FM与SVM区别                                                  |                                                              |              |                                                              |            |
| 原理           | 三种方式：Bagging, Boosting, Stacking                        |                                                              |              |                                                              |            |
| 原理           | XGBoost原理                                                  |                                                              |              |                                                              |            |
| 原理           | LightGBM = XGBoost + Histogram + GOSS + EFB                  |                                                              |              |                                                              |            |
| 原理           | CatBoost = Catgorical + Boost                                |                                                              |              |                                                              |            |
| 原理           | 自然梯度理解                                                 |                                                              |              |                                                              |            |
| 工具           | XGBoost，LightGBM, CatBoost工具使用                          |                                                              |              |                                                              |            |
| 工具           | 调试工程 Debug能力                                           |                                                              |              |                                                              |            |
| 课下思考与练习 |                                                              |                                                              |              |                                                              |            |
| Thinking1      | XGBoost与GBDT的区别是什么？                                  |                                                              |              | 简要说明这两者之间的区别（10points）                         |            |
| Thinking1      | 举一个你之前做过的预测例子（用的什么模型，解决什么问题，比如我用LR模型，对员工离职进行了预测，效果如何...  请分享到课程微信群中） | 简要说明之前做过的例子，用的模型，解决的问题，并且在群里分享（10points） |              |                                                              |            |
| Thinking2      | 请你思考，在你的工作中，需要构建哪些特征（比如用户画像，item特征...），这些特征都包括哪些维度（鼓励分享到微信群中，进行交流） | 能对工作场景，以及构造的特征进行洞察，在班级群中分享（10points） |              |                                                              |            |
| Action1        | 男女声音识别     数据集：voice.csv     3168个录制的声音样本（来自男性和女性演讲者），采集的频率范围是0hz-280hz，已经对数据进行了预处理     一共有21个属性值，请判断该声音是男还是女？     使用Accuracy作为评价标准 |                                                              |              | 1、完成代码（30points）     2、分享经验（30points）     3、得分Top3（10points） |            |