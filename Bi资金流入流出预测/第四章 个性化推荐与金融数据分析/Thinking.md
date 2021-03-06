#### Thinking1  如果你是某P2P租车的技术负责人，你会如何设计个性化推荐和搜索排序     阐述相似车型，搜索排序的设计方法     可能的embedding策略

阐述相似车型，搜索排序的设计方法
可能的embedding策略

特征梳理：

1. 车辆信息：包括车型，颜色，排量，油耗等
2. 用户信息：包括用户所在地，性别，工作，薪资等

特征融合：将特征进行embedding：

1. 将车辆信息和用户信息做为节点，将同一车辆的信息进行连接，同一用户的信息进行连接，将历史租车数据中的车型与用户相连，形成图结构，使用node2vec进行图结构的embedding
2. 将同一用户的租车型号进行连接，将租同一型号车的用户相连，形成图结构，分别进行用户和车型的embedding，将当前用户和车型embedding进行拼接

车型推荐：将embedding信息输入预测模型，预测用户租车的概率




| 分类           | 内容                                                         | 数据集 | 是否了解掌握 | 评阅点                                                       | GitHub代码 |
| -------------- | ------------------------------------------------------------ | ------ | ------------ | ------------------------------------------------------------ | ---------- |
| 课上理解部分   |                                                              |        |              |                                                              |            |
| 原理           | Airbnb个性化推荐使用场景                                     |        |              |                                                              |            |
| 原理           | List Embedding构造（Search  Ranking, d32 reg, d32 book, d32 book neg） |        |              |                                                              |            |
| 原理           | List Embedding评估                                           |        |              |                                                              |            |
| 原理           | Type Embedding构造                                           |        |              |                                                              |            |
| 原理           | 基于Embedding的实时个性化                                    |        |              |                                                              |            |
| 工具           | Project A：信用卡违约预测                                    |        |              |                                                              |            |
| 工具           | Project B：信用卡欺诈预测                                    |        |              |                                                              |            |
| 工具           | GridSearchCV使用                                             |        |              |                                                              |            |
| 工具           | Pipeline使用                                                 |        |              |                                                              |            |
| 原理           | Fintech应用场景                                              |        |              |                                                              |            |
| 原理           | Fintech公司&人才发展                                         |        |              |                                                              |            |
| 原理           | 如何使用Python进行量化交易                                   |        |              |                                                              |            |
| 课下思考与练习 |                                                              |        |              |                                                              |            |
| Thinking1      | 如果你是某P2P租车的技术负责人，你会如何设计个性化推荐和搜索排序     阐述相似车型，搜索排序的设计方法     可能的embedding策略 |        |              | 能简要阐述相似车型，搜索排序的方法（10points）     能简要阐述可能的embedding策略（10points） |            |
| Action1        | 信用卡违约率检测     https://www.kaggle.com/uciml/default-of-credit-card-clients-dataset     对信用卡使用数据进行建模，预测用户是否下个月产生违约 => 分类问题     机器学习算法有很多，比如SVM、决策树、随机森林和KNN => 该使用哪个模型     可以使用GridSearchCV工具，找到每个分类器的最优参数和最优分数，最终找到最适合数据集的分类器和此分类器的参数 |        |              | 1、完成代码（10points）     2、使用GridSearchCV，多种分类器（20points）     3、使用Pipeline（10points） |            |
| Action2        | 信用卡欺诈分析：     数据集：2013年9月份两天时间内的信用卡交易数据     284807笔交易，492笔欺诈行为     https://www.kaggle.com/mlg-ulb/creditcardfraud     数据样本包括了28个特征V1，V2，……V28，以及交易时间Time和交易金额Amount     因为数据隐私，28个特征值是通过PCA变换得到的结果。     需要预测 每笔交易的分类Class，该笔交易是否为欺诈     Class=0为正常（非欺诈），Class=1代表欺诈 |        |              | 1、数据探索可视化（20points）     2、模型训练及结果预测（20points） |            |