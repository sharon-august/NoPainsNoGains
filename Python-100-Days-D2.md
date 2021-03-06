## 一、进制转换（十进制D，二进制B，八进制Q，十六进制H）
### 1.十进制正数
（1）k转十：位权法或指数求和法。公式：abcd.efg = d * k^0 + c * k^1 + b * k^2 + a * k^3 + e * k^(-1) + f * k^(-2) + g * k^(-3)

（2）十转k  
整数，除k取余，倒序排列。  
小数，乘k取整，正序排列。用k乘小数部分，将积的整数部分取出，再用k乘余下的小数部分，再将积的整数部分取出，如此进行，直到积中的小数部分为零，或者达到所要求的精度为止（有时是无限位）。  
e.g. 10.68D = 12.534Q（精确到小数点后3位）, 25.68D = 19.ae1H（精确到小数点后3位）

### 2.二进制与八进制
B转Q：三合一法。e.g. 1010 0100B = 244Q  
Q转B：一分三法

### 3.二进制与十六进制
B转H：四合一法。e.g. 1010 0100B = a4H  
H转B：一分四法

转换表：  
位数 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 |
---- |---- |---- |---- |---- |---- |---- |---- |---- |
B | 1 | 1 | 1 | 1 | 1 | 1 | 1 | 1 |
D | 128 | 64 | 32 | 16 | 8 | 4 | 2 | 1 |

对照上表拆分。e.g. 135D = 128D + 7D = 128D + 4D + 2D + 1D = 1000 0111B

参考：[计算机基础进制转换（二进制、八进制、十进制、十六进制）](https://blog.csdn.net/yuanxiang01/article/details/82503568?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-1.nonecase&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-1.nonecase)

### 4.十进制负数：先转为二进制
（1）D转B：  
1）绝对值转为B；  
2）高位补零，补齐32位，符号位（最高位）取1，得到原码；  
3）除符号位外，各位取反，末位加1。  
e.g. -5D = 11111111 11111111 11111111 11111011B = ff ff ff fbH

（2）B转D：符号位为1的二进制数，末位减1，除符号位外各位取反，得到原码，再转为十进制。  
参考：[十进制负数转二进制](https://blog.csdn.net/LaoXiangQ/article/details/86645513)



## 二、语言元素
### 1.逻辑运算符的使用
输入年份判断是否为闰年  
```
year = int(input('请输入年份：'))
is_leap = year % 4 == 0 and year % 100 != 0 or year % 400 == 0
print('闰年：', is_leap)
# 2005只用D1（and左边是false，短路处理），2020用到D2（or左边是true，短路处理）, 1900和2000用到D3
```

### 2.常用函数
* input()  
input('a = ') 显示引号内的内容，读取键盘输入的内容为字符串，以回车键结束

* print()  
print('%.1f华氏度 = %.1f摄氏度' % (F_deg, C_deg))输出带占位符的字符串，保留1位小数  
print('%d %% %d = %d' % (a, b, a % b)) **取余**  
print('%d // %d = %d' % (a, b, a // b)) **整除**  
**占位符：%d整数，%f小数**  
**占位输出的真值是表达式或多个值时要用括号括起来，单个变量不用括**  
e.g. print('周长 = %.2f' % (a + b + c))， print('面积 = %.2f' % area)  
flag2 = 2 < 1;print(flag2 is not False)打印表达式的结果False（is为身份运算符）

* int()：将一个数值或字符串转换成整数，可以指定进制  
能把str型'17'转换为整数17，但不能把字母a转为ASCII码97

* float()：将一个字符串转换成浮点数  
* str()：将指定的对象转换成字符串形式，可以指定编码  
* chr()：将整数转换成该编码对应的字符串（一个字符）  
* ord()：将字符串（一个字符）转换成对应的编码（整数） 
* bool()：将字符串转换为bool型
* type()：数据类型

[运算符及优先级表](https://github.com/jackfrued/Python-100-Days/blob/master/Day01-15/02.%E8%AF%AD%E8%A8%80%E5%85%83%E7%B4%A0.md)

扩展：[Python将'\u'开头的字符串转为unicode编码](https://blog.csdn.net/xw_classmate/article/details/51935105)  
[汉字转化unicode编码在线工具](http://www.bangnishouji.com/tools/chtounicode.html)  
```
str3 = '\u6768\u7ecd\u7eaf'
print(str3)
# 输出：杨绍纯
```
