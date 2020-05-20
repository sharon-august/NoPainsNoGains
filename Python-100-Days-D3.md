## 分支结构
#### 1.Python之禅：Flat is better than nested.
用扁平结构if...elif...else 比 嵌套结构if...else:if...else可读性高

#### 2.判断是否在区间内的正确写法
if 90 <= score <= 100:而不是if score <= 100 and score >= 90:

#### 3.分支结构中的print
若各个分支输出的式子不同，则每个分之内用print，否则只在分支结构结束后才print，各分支内用一个变量代替


#### 其他：常用函数
（1）求平方：** 0.5，也可先 import math, 再用math.sqrt()  
（2）random.randint(a, b)返回随机整数 N 满足 a <= N <= b  
（3）getpass.getpass(prompt='Password: ', stream=None)  
提示用户输入一个密码且不会回显。 用户会看到字符串 prompt 作为提示，其默认值为 'Password: '。 在 Unix 上，如有必要提示会使用替换错误句柄写入到文件类对象 stream。 stream 默认指向控制终端 (/dev/tty)，如果不可用则指向 sys.stderr (此参数在 Windows 上会被忽略)。  
e.g. import getpass  
...  
password = getpass.getpass("请输入密码：")  
（貌似没什么用，而且Warning: Password input may be echoed.）

参考：[Python3.7文档](https://docs.python.org/3.7/)
