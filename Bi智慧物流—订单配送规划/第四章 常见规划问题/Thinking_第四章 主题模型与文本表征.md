[TOC]



# 第四章 主题模型与文本表征

### Thinking1  对于同一个带约束的规划问题，LP和MIP哪个运算复杂度高，为什么？      

能简要说明两者之间的区别及运算复杂度（10points）    

MIP：Mixed Integer Programming 混合整数规划，混合整数规划是LP的一种，其中部分的决策变量是整数（不要求全部都是整数）

LP：Linear Programming 线性规划，研究线性约束条件下线性目标函数的极值问题

* MIP复杂度更高，必须符合约束条件下，类似于穷举；决策变量部分是整数，不要求全部都是整数的规划问题
* LP相比MIP复杂度低，因为它有数学优化在里面，不需要满足一些整数约束条件



### Thinking2  TSP与VRP问题的关系是怎样的？      

能简要说明TSP与VRP的关系（10points）

* 旅行商问题（TSP）：

  Travelling Salesman Problem，一个旅行商想去拜访若干城市，然后回到他的出发地，给定各个城市之间所需的旅行时间后，怎样计划他的路线，使得他能对每个城市恰好进行一次访问，而且总时间最短

* 多回路运输问题（VRP）:

  Vehicle Routing Problem 车辆路径问题，可以看成**旅行商问题的推广**

  它是指一定数量的客户，各自有不同数量的货物需求，配送中心向客户提供货物，由一个车队负责分送货物，组织适当的行车路线，**目标**是使得客户的需求得到满足，并能在一定的约束下，达到诸如**路程最短、成本最小、耗费时间最少**等目的

  

| 分类           | 内容                                                         | 数据集 | 是否了解掌握 | 评阅点                                                       | GitHub代码 |
| -------------- | ------------------------------------------------------------ | ------ | ------------ | ------------------------------------------------------------ | ---------- |
| 课上理解部分   |                                                              |        |              |                                                              |            |
| 原理           | 线性规划                                                     |        |              |                                                              |            |
| 原理           | 整数规划                                                     |        |              |                                                              |            |
| 原理           | 混合整数规划                                                 |        |              |                                                              |            |
| 工具           | pulp工具                                                     |        |              |                                                              |            |
| 工具           | Google ortools                                               |        |              |                                                              |            |
| 原理           | TSP                                                          |        |              |                                                              |            |
| 原理           | VRP                                                          |        |              |                                                              |            |
| 课下思考与练习 |                                                              |        |              |                                                              |            |
| Thinking1      | 对于同一个带约束的规划问题，LP和MIP哪个运算复杂度高，为什么？ |        |              | 能简要说明两者之间的区别及运算复杂度（10points）             |            |
| Thinking2      | TSP与VRP问题的关系是怎样的？                                 |        |              | 能简要说明TSP与VRP的关系（10points）                         |            |
| Action1        | Santa的接待安排     圣诞节前100天，Santa开放了workshop，欢迎以家庭单位的参观，如何更合理的安排这些家庭参观？     每个家庭有10个选择choice0-9，数字代表了距离圣诞节的天数，比如 1代表12月24日，每个家庭必须并且只安排一次参观     家庭数量 5000，即family_id 为[0, 4999]，每天访问的人数需要在125-300人     为了更合理的计算Santa的安排能力，我们使用preference cost和accounting penalty两个指标     1）preference cost，代表Santa的个性化安排能力     2）accounting penalty，代表Santa安排的财务成本     每天接待的人员数N(d)如果大于125，就会拥挤，产生过多的清洁成本     最终的 Score = preference cost + accounting penalty     最终提交每个家庭的安排 submission.csv |        |              | 1、使用LP对大部分家庭进行安排（30points）     2、使用MIP对剩余家庭进行安排（30points）     3、对得到的解决方案进行优化（20points） |            |