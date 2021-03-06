[TOC]

# 第五章 常见规划问题2

### Thinking1  线性规划与混合整数规划的区别是什么？      

能简要说明两者之间的区别（10points）

* 区别在于线性规划的决策变量无整数限制，而混合整数规划是线性规划的一种，其部分的决策变量是整数（不要求全部都是整数）。


###  Thinking2  针对VRP问题，常见的约束条件都有哪些？      

能简要说明VRP问题中常见的约束条件（10points）

* 常见约束条件如：物需求量、发送量、交发货时间、车辆容量限制、行驶里程限制、时间限制、车辆最大行驶距离等

| 分类           | 内容                                                         | 数据集 | 是否了解掌握 | 评阅点                                                       | GitHub代码 |
| -------------- | ------------------------------------------------------------ | ------ | ------------ | ------------------------------------------------------------ | ---------- |
| 课上理解部分   |                                                              |        |              |                                                              |            |
| 原理           | 线性规划                                                     |        |              |                                                              |            |
| 原理           | 整数规划                                                     |        |              |                                                              |            |
| 原理           | 混合整数规划                                                 |        |              |                                                              |            |
| 工具           | Google ortools                                               |        |              |                                                              |            |
| 原理           | TSP                                                          |        |              |                                                              |            |
| 原理           | VRP                                                          |        |              |                                                              |            |
| 原理           | CVRP（带约束条件的VRP）                                      |        |              |                                                              |            |
| 工具           | VRP工具（RoutingModel）                                      |        |              |                                                              |            |
| 课下思考与练习 |                                                              |        |              |                                                              |            |
| Thinking1      | 线性规划与混合整数规划的区别是什么？                         |        |              | 能简要说明两者之间的区别（10points）                         |            |
| Thinking2      | 针对VRP问题，常见的约束条件都有哪些？                        |        |              | 能简要说明VRP问题中常见的约束条件（10points）                |            |
| Action1        | Santa的接待安排     圣诞节前100天，Santa开放了workshop，欢迎以家庭单位的参观，如何更合理的安排这些家庭参观？     每个家庭有10个选择choice0-9，数字代表了距离圣诞节的天数，比如 1代表12月24日，每个家庭必须并且只安排一次参观     家庭数量 5000，即family_id 为[0, 4999]，每天访问的人数需要在125-300人     为了更合理的计算Santa的安排能力，我们使用preference cost和accounting penalty两个指标     1）preference cost，代表Santa的个性化安排能力     2）accounting penalty，代表Santa安排的财务成本     每天接待的人员数N(d)如果大于125，就会拥挤，产生过多的清洁成本     最终的 Score = preference cost + accounting penalty     最终提交每个家庭的安排 submission.csv |        |              | 1、使用LP对大部分家庭进行安排（20points）     2、使用MIP对剩余家庭进行安排（20points）     3、对得到的解决方案进行优化（10points） |            |
| Action2        | 多辆车的路径规划 VRP：     条件：经过中国33个城市，一共4辆车，每辆车最大行驶10000公里     目标：使得每辆车的行驶里程数更接近     需要注意：     1）在VRP问题中，路径上给点赋的index和点实际的index不一样，需要使用IndexToNode方法进行转换才能得到实际的index |        |              | 1、完成带有约束条件的VRP问题（20points）     2、结果正确（10points） |            |