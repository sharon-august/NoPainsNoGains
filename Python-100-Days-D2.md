## 一、进制转换（十进制D，二进制B，八进制Q，十六进制H）
### 1.十进制
（1）k转十：位权法或指数求和法
公式：abcd.efg = d * k^0 + c * k^1 + b * k^2 + a * k^3 + e * k^(-1) + f * k^(-2) + g * k^(-3)

（2）十转k
正整数，除k取余，倒序排列
负整数，
小数，乘k取整，正序排列。用k乘小数部分，将积的整数部分取出，再用k乘余下的小数部分，再将积的整数部分取出，如此进行，直到积中的小数部分为零，或者达到所要求的精度为止（有时是无限位）。
e.g. 10.68D = 12.534Q（精确到小数点后3位）, 25.68D = 19.ae1H（精确到小数点后3位）

### 2.二进制与八进制
B转Q：三合一法。e.g. 1010 0100B = 244Q
Q转B：一分三法

### 3.二进制与十六进制
B转H：四合一法。e.g. 1010 0100B = a4H
H转B：一分四法

参考：[计算机基础进制转换（二进制、八进制、十进制、十六进制）](https://blog.csdn.net/yuanxiang01/article/details/82503568?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-1.nonecase&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-1.nonecase)
