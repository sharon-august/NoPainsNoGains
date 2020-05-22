## 循环结构
1.类型：for-in循环和while循环 
for _ in range(n)中 _ 占位符,表示不在意变量的值 只是用于循环遍历n次，无法打印变量值。  
for i in range(n) 在意变量i的值 可以打印print(i)  
例如在一个序列中只想取头和尾，就可以使用_  
```
nums = (1,2,3,4,5,6,7,8,9)
head,*_,tail = nums
print(head)
print(tail)
```

2.break：提前终止循环。只能终止它所在的那个循环，这一点在嵌套的循环结构中尤其要注意。  
continue：放弃本次循环后续的代码直接让循环进入下一轮。

#### 数学常识
1.素数指的是只能被1和自身整除的大于1的整数  
判断一个正整数是不是素数：只要判断2到sqrt(num)之间的数能否整除num

2.两个数的最大公约数是两个数的公共因子中最大的那个数；两个数的最小公倍数则是能够同时被两个数整除的最小的那个数。  
思路：从较小的数开始除，能整除的就是最大公约数，最小公倍数=x * y//最大公约数。没有公约数时，最大公约数为1，最小公倍数为x * y。

#### 常用函数及语法
1.range: a sequence of integers from start (inclusive) to stop (exclusive) by step.  
e.g. range(i, j) produces i, i+1, i+2, ..., j-1.  
start defaults to 0, and stop is omitted! range(4) produces 0, 1, 2, 3.  
range(100, 0, -2)：产生100到1的偶数，其中-2是步长，即每次数字递减的值。

2.交换：x, y = y, x

#### pycharm快捷键
Ctrl+Q：调出快速文档  
三击：选中整行  
Shift+Alt+E：在console中执行选中内容  
Shift+F6或Ctrl+Shift+Alt+J：批量修改变量名  
Ctrl+F12：变量导航
