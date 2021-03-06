### Thinking1  奇异值分解SVD的原理是怎样的，都有哪些应用场景      1、能简单说明奇异值分解的原理（5points）     2、举例说明两个以上的使用场景（5points)   

1. 原理：将一个矩阵分解为三个矩阵相乘的形式，特征向量矩阵 * 特征值矩阵 * 特征向量矩阵转置，通过减少特征值矩阵的维度从而达到缺失值填充或数据降维的效果。
2. 应用场景举例：推荐系统：降维、数据填充；图像压缩：降维

###   Thinking2  funkSVD, BiasSVD，SVD++算法之间的区别是怎样的      1、能简述3种算法之间的差异（10points)    

1. funkSVD对比SVD，通过损失函数最小化，优化最佳填充值
2. BiasSVD对比FunkSVD，其损失函数加入用户偏好，进行加入用户偏好的填充值优化
3. SVD++对比BiasSBD，其损失函数加入用户隐式反馈（没有具体的评分，但可能有点击，浏览等行为），然后最优化损失函数

### Thinking3  矩阵分解算法在推荐系统中有哪些应用场景，存在哪些不足      1、能说明推荐系统中的典型应用场景（5points）     2、MF在推荐系统中的局限性（5points）    

1. 应用场景：填充缺失值；降维

2. MF局限性：提取特征少，只用了两个维度的信息，导致泛化能力差；可解释性差

### Thinking4  假设一个小说网站，有N部小说，每部小说都有摘要描述。如何针对该网站制定基于内容的推荐系统，即用户看了某部小说后，推荐其他相关的小说。原理和步骤是怎样的  能简要说明基于内容进行推荐的步骤及原理（10points)        

* 原理：计算当前小说特征向量与整个小说特征矩阵的余弦相似度，取相似度最大的Top-k个
  1. 对小说的描述进行特征提取：N-Gram、TF-IDF
  2. 计算小说描述之间的相似度矩阵，求某id与矩阵的余弦相似度
  3. 选择Top-k个输出

### Thinking5  Word2Vec的应用场景有哪些      能说明在NLP和推荐系统中的应用场景（10points）    

1. NLP：作为cnn、rnn、lstm等深度学习神经网络的输入；词之间相似度分析；作为文本情感分类、机器翻译、文本生成等等nlp领域的输入项
2. 推荐系统：方便计算词或文章之间的相似度以此做内容推荐

### Action1  选择任意一张图片，对其进行灰度化，然后使用SVD进行图像的重构，当奇异值数量为原有的1%，10%，50%时，输出重构后的图像      1、完成代码，结果正确（10points）    

### Action2  使用Google  Colab编辑器，对MovieLens数据集进行评分预测，计算RMSE（使用funkSVD, BiasSVD，SVD++）      1、使用Colab完成3种算法在MovieLens的评分预测（20points）     2、使用Surprise以外的工具(+5points)    

### Action3  使用Gensim中的Word2Vec对三国演义进行Word  Embedding，分析和曹操最相近的词有哪些，曹操+刘备-张飞=?     数据集：three_kingdoms.txt      1、完成代码，结果正确（20points）




| 分类           | 内容                                                         | 数据集                                            | 是否了解掌握 | 评阅点                                                       | GitHub代码 |
| -------------- | ------------------------------------------------------------ | ------------------------------------------------- | ------------ | ------------------------------------------------------------ | ---------- |
| 课上理解部分   |                                                              |                                                   |              |                                                              |            |
| 原理           | 常用的推荐算法都有哪些（SVD算法在推荐系统算法中的位置）      |                                                   |              |                                                              |            |
| 原理           | 普通矩阵分解原理                                             |                                                   |              |                                                              |            |
| 原理           | 对称矩阵分解原理                                             |                                                   |              |                                                              |            |
| 原理           | 奇异值分解SVD原理                                            |                                                   |              |                                                              |            |
| 工具           | 如何使用Python进行SVD分解                                    |                                                   |              |                                                              |            |
| 工具           | 使用SVD对图像进行压缩重构                                    |                                                   |              |                                                              |            |
| 原理           | 传统SVD在推荐系统中的应用功能                                |                                                   |              |                                                              |            |
| 原理           | funkSVD算法原理                                              |                                                   |              |                                                              |            |
| 原理           | BiasSVD算法原理                                              |                                                   |              |                                                              |            |
| 原理           | SVD++算法原理                                                |                                                   |              |                                                              |            |
| 工具           | Surprise中对应的SVD工具                                      | MovieLens                                         |              |                                                              |            |
| 工具           | Google Colab编辑器                                           |                                                   |              |                                                              |            |
| 原理           | 基于内容的推荐（为酒店建立内容推荐系统）                     |                                                   |              |                                                              |            |
| 原理           | 什么是N-Gram                                                 |                                                   |              |                                                              |            |
| 原理           | 余弦相似度计算                                               |                                                   |              |                                                              |            |
| 工具           | CountVectorizer与TfidfVectorizer                             |                                                   |              |                                                              |            |
| 原理           | Word Embedding                                               |                                                   |              |                                                              |            |
| 课下思考与练习 |                                                              |                                                   |              |                                                              |            |
| Thinking1      | 奇异值分解SVD的原理是怎样的，都有哪些应用场景                |                                                   |              | 1、能简单说明奇异值分解的原理（5points）     2、举例说明两个以上的使用场景（5points) |            |
| Thinking2      | funkSVD, BiasSVD，SVD++算法之间的区别是怎样的                |                                                   |              | 1、能简述3种算法之间的差异（10points)                        |            |
| Thinking3      | 矩阵分解算法在推荐系统中有哪些应用场景，存在哪些不足         |                                                   |              | 1、能说明推荐系统中的典型应用场景（5points）     2、MF在推荐系统中的局限性（5points） |            |
| Thinking4      | 假设一个小说网站，有N部小说，每部小说都有摘要描述。如何针对该网站制定基于内容的推荐系统，即用户看了某部小说后，推荐其他相关的小说。原理和步骤是怎样的 | 能简要说明基于内容进行推荐的步骤及原理（10points) |              |                                                              |            |
| Thinking5      | Word2Vec的应用场景有哪些                                     |                                                   |              | 能说明在NLP和推荐系统中的应用场景（10points）                |            |
| Action1        | 选择任意一张图片，对其进行灰度化，然后使用SVD进行图像的重构，当奇异值数量为原有的1%，10%，50%时，输出重构后的图像 |                                                   |              | 1、完成代码，结果正确（10points）                            |            |
| Action2        | 使用Google  Colab编辑器，对MovieLens数据集进行评分预测，计算RMSE（使用funkSVD, BiasSVD，SVD++） |                                                   |              | 1、使用Colab完成3种算法在MovieLens的评分预测（20points）     2、使用Surprise以外的工具(+5points) |            |
| Action3        | 使用Gensim中的Word2Vec对三国演义进行Word  Embedding，分析和曹操最相近的词有哪些，曹操+刘备-张飞=?     数据集：three_kingdoms.txt |                                                   |              | 1、完成代码，结果正确（20points）                            |            |