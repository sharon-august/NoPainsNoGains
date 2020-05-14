## 分支结构
#### 1.Python之禅：Flat is better than nested.
用扁平结构if...elif...else 比 嵌套结构if...else:if...else可读性高

#### 2.判断是否在区间内的正确写法
if 90 <= score <= 100:而不是if score <= 100 and score >= 90:

#### 3.分值结构中的print
若各个分支输出的式子不同，则每个分之内用print，否则只在分支结构结束后才print，各分支内用一个变量代替


#### 其他
（1）求平方：** 0.5，也可先 import math, 再用math.sqrt  
（2）random.randint(a, b)返回随机整数 N 满足 a <= N <= b  
