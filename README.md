# cs551 Project 1
# Lead Director: Xinyu Li (Boss Li)

## Features

### Basic Feature: (163个)

1. children: numeric
2. controversiality: categorical -> numeric
3. isRoot: categorical -> numeric {1, 0}
4. 160个词频统计

### Additional Features: (5个)

- 词性统计(多少个名词/动词, 占整个文章长度的比重)
  - count(名词)/len(评论)
  - count(动词)/len(评论)
  - 前面两个的interaction effect
  - 一个问题, 上面这些会不会和那160个有关联? 
  
- 是否包含URL: categorical -> numeric {1, 0}

- Children和isRoot的interaction
  - 似乎大家都喜欢(也只有耐心看)在第一个评论下写东西吧...

...未完待续

## 实验

### 必须

- 比较直接计算和梯度下降的
  - 运行时间
  - 稳定性
  - 准确性
  忽略160个feature, 试用不同的学习速率
- 测试0, 60, 160个feature的区别
- 测试加进去的几个feature
- 过测试

### 附加

- 应用backward selection筛选feature
  - 算不过来就减少, 但一定要做出来
- 在基础特征1, 2, 3和附加特征1-1, 1-2, 2, 3上实验polynomial feature
  - degree再议
- 试图比较NLTK去掉stop word和不去掉stop word的精确度
