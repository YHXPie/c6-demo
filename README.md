_必修一  程序设计语言_
## Python 相关
所有内容均来源自《必修一 数据与计算知识点刚要》，仅用作整理用途。如果你不想看那本纲要知识点，欢迎浏览或者打印本页。

!> **注意：在 Python 中，所有的符号都是英文符号！**
- - - -
### 目录
1. [ **Python 基础知识** ](/?id=_1-python-基础知识)
- 1.1 [常量与变量](/?id=_11-常量与变量)
- 1.2 [数据类型](/?id=_12-数据类型)
- 1.3 [运算符](/?id=_13-运算符)
- 1.4 [表达式](/?id=_14-表达式)
- 1.5 [函数](/?id=_15-函数)
2. [ **Python 语句** ](/?id=_2-python-语句)
- 2.1 [赋值语句](/?id=_21-赋值语句)
- 2.2 [输入语句](/?id=_22-输入语句)
- 2.3 [输出语句](/?id=_23-输出语句)
- 2.4 [列表操作语句](/?id=_24-列表操作语句)
- 2.5 [注释语句](/?id=_25-注释语句)
- 2.6 [分支语句](/?id=_26-分支语句)
- 2.7 [循环语句](/?id=_27-循环语句)
- 2.8 [自定义函数](/?id=_28-自定义函数)
- - - -
### 1. Python 基础知识
#### 1.1 常量与变量
**常量：** 在程序运行过程中值始终保持不变的量，通常是固定的数值或字符串。例如 `3.14` `'hello'`。

**变量：** 在程序运行过程中值允许改变的量。Python 中的变量不需要先定义，根据其赋予的值来确定其数据类型。

?> **变量的命名规则：** 必须以字母或下划线开头，后面可以是字母、数字或下划线；变量名区分大小写，同时不能使用系统保留字，如 `if` `for` `False` `True` `def` 等。

#### 1.2 数据类型
Python 的常用数据类型有 **`Number`（数值）、`String`（字符串）、`List`（列表）** 等。其中，数值型又可分为 **整型 `int` 和浮点型 `float`** 。数据类型之间可以进行转换，例如 `int( )` `float( )` `str( )` 等。

例如：

输入：
```Python
a = int(123.456)
print(a)
```
Python输出：
```Python(IDLE)
123
```
再或者，输入：
```Python
a = str(123.456)
print(a)
```
Python输出：
```Python(IDLE)
123.456
```
#### 1.3 运算符 
- **算术运算符：** 加 `+`、减`-`、乘`*`、幂`**`、除`/`、整除`//`、取余`%`。
- **关系运算符：** 等于`==`、大于`>`、大于等于`>=`、小于`<`、小于等于`<=`、不等于`!=`。
- **逻辑运算符：** 与`and`、或`or`、非`not`。
- **赋值运算符：** `=`、`+=`、`-=`、`*=`、`/=`。例如，x+=y 相当于 x=x+y。

!> **`==`这类符号中间没有空格。** 如果加上空格，Python会进行报错。如下所示：
```Python(IDLE)
#正常运算
1+2==3
True

#错误运算
1+2= =3
SyntaxError: cannot assign to expression
```
#### 1.4 表达式
?> 由关系运算符连接而成的表达式称为关系表达式；由逻辑运算符连接而成的表达式称为逻辑表达式。

当一个表达式中有多种运算符时，运算的顺序将根据运算符的优先级由高到低进行运算，如果是同级运算则按从左到右的顺序进行。

Python 常用运算符优先级如下：**>算术运算符>关系运算符>赋值运算符>逻辑运算符。

#### 1.5 函数
函数可分为系统函数和用户自定义函数两种类型。

**系统函数**

即函数库里的标准函数,是程序设计语言或操作系统提供给用户的一系列已经编写好的程序。如 `print()`函数和 `input()`函数等。

**用户自定义函数**

即用户自己编写的程序代码。定义格式等详见 2.8。
- - - -
### 2. Python 语句
#### 2.1 赋值语句 
一般格式为：

`变量=表达式`

?> 在 Python 中,赋值符号不是等号，具有 **方向性**，由右边赋给左边，赋值号`=`左边**只能是变量**。

例如：
```Python
a=3  
#将 3 赋值给变量 a 

n=n+1 
#先计算赋值号右边的表达式 n+1,再将计算后的值赋给左边的变量 n

a=b=c=1 
#数值 1 赋值给变量 a,b,c

a,b,c=1,2,3 
#数值 1,2,3 分别赋值给变量 a,b,c

a,b=b,a 
#交换 a,b 两个变量的值
```
#### 2.2 输入语句 
一般格式为：
`<变量>=input("提示信息：")`
?> input()函数的返回结果都是字符串。

例如：
```python
age=int(input(“请输入年龄：”))
#将输入的年龄数据转换为整数赋值给变量age。
```
#### 2.3 输出语句 
一般格式为：

`print([object,…][,sep=’’][,end='\n'])`

_方括号中的项是可选的，可以省略，如省略则取系统的默认值。这些内容应该不需要过多了解，原文见下：_

> `object`是要输出的对象，可以是常量、变量或表达式等。
> 
> `sep`后面的空格（可以指定为其他字符）表示每个输出对象之间的分隔符，如缺省默认值是一个单个的空格。
> 
> `end`后面的字符串含义为输出文本尾的一个字符串，如缺省默认值是一个`\n`换行符。如`end=' '`，表示输出当前行的所有内容后，在末尾加一个空格，不换行接着输出下一个`print()`的输出对象。

##### 格式化输出
`%`用法:实现整数的输出、浮点数输出、字符串输出。

用法如下：
- `%d`，十进制
- `%x`，十六进制
- `%f`，保留小数点后面六位有效数字
- `%.3f`，保留 3 位小数位

语法：
```Python
print('_'%_)
```
第一个_填写格式化输出的参数，第二个_填写要输出的量。

例如：
```Python
x = int(123.456)
print('%x'%x)
```
输出：
```Python(IDLE)
7b
```
再或者：
```Python
x = 123.45678901
print('%.4f'%x)
```
输出：
```Python(IDLE)
123.4568
```
!> 如果要自定义保留的小数点位数，使用参数`'%.Xf'%`，其中`X`表示要保留的小数点位数。默认情况下，使用参数`'%f'%`会保留6 位小数位。例如：
```Python
x = 123.45678901
print('%f'%x)
```
输出：
```Python(IDLE)
123.456789
```
##### `{}.format` 用法
该函数把字符串当成一个模板，通过传入的参数进行格式化，基本语法是通过 `{}` 和`:`来代替以前的`%`。

_由于几乎不可能会用到而且不太会，暂时不讲这一部分。_

#### 2.4 列表操作语句 
列表是包含多个元素的有序集合。列表元素写在方括号`[]`之间，用逗号分隔开。列表常用操作如下：
- 建立空列表：`list=[]`
- 末尾追加元素：`list.append()`
- 删除末尾元素：`list.pop()`
- 插入元素：`list.insert()`
- 删除元素：`list.remove()`或`del list[]`
- 列表排序：`list.sort()`
- 列表逆序：`list.reverse()`
- 返回索引：`list.index()`
- 正负索引：从左往右第一个元素索引号为 0；从右往左第一个元素索引号为-1。

#### 2.5 注释语句 
python 中的注释有单行注释和多行注释。单行注释以#开头；多行注释用三个单引号'''或者三个双引号"""将注释括起来。注释只是用来方便自己或其他人读懂代码，不会被程序
执行。
```
# 这是单行注释

'''
这是多行注释
这是多行注释
'''
```
!> 使用多行注释时，请确保前后使用的引号一致！

#### 2.6 分支语句 
?> if（条件表达式）后面加冒号`:`。且当语句 A 是由多个语句构成的复合语句时，所有语句严格遵循相同的缩进。如下示例：
```Python
if score>100 or score<0:
    print("你的成绩输入有误")
    print("请重新输入")
#这段代码仅供参考，实际上你不必连用两个 Print 函数。
```
##### 单分支 if 语句
一般格式为：
```
if(条件表达式):
  语句 A
```
例如：输入两个整数 a、b，分别输出大数和小数。
```Python
a=int(input("输入一个数 a 是："))
b=int(input("输入一个数 b 是："))
if a<b:
    a,b= ① 
print("大数是", ② ,"小数是", ③ )
```
##### 双分支 if 语句
一般格式为：
```
if(条件表达式)：
  语句 A
else:
  语句 B
```
例如：输入一个正整数 n，判断其奇偶性。
```Python
n = int(input("输入一个正整数: "))
if ① :
     print(n,"是偶数")
else:
     print( ② )
```
##### 多分支 if…elif…else 语句
?> 该语句以`if`开头，以`else`结束。
一般格式为：
```
if 表达式 1：
    语句块 1
elif 表达式 2：
    语句块 2
    ……
elif 表达式 n：
    语句块 n
else:
    语句块 n+1
```
#### 2.7 循环语句 
##### 计数循环 for 语句
一般格式为：
```
for 循环变量 in 列表：
    语句或语句组
```
?> for 循环中冒号`:`代表下一行是循环的第一行。注意循环体在书写时需要缩进。从 for 语句末尾的冒号开始至其下面没有缩进的代码之间都是其包含的需要重复执行的部分。

在 for 语句中，in 后也可以是 range()函数，它可以生成某个范围内的数字列表。

语法：

`range(start,stop[,step])`

参数说明：
- **start：** 计数从 start 开始。默认是从 0 开始。例如：`range(5)`等价于 `range(0,5)`。
- **stop：** 计数到 stop 结束，但不包括 stop。例如：`range(0,5)`是 0,1,2,3,4 **没有 5。**
- **step：** 步长，默认为 1。例如：r`ange(0,5)`等价于 `range(0,5,1)`。

##### 条件循环 while
一般格式为：
```
while 关系表达式：
    语句或语句组
```

?> 当表达式的值为真时，执行循环体语句；当表达式的值为假时，退出循环，执行循环体外的下一条语句(即 while 后面没有缩进的第一条语句)。每次循环都是执行完循环体语句后回到表达式处重新开始判断，重新计算表达式的值。

!> 注意循环体中必须有改变条件表达式值的语句，否则将成为死循环。
##### 循环嵌套
如果某一种循环语句中包含着自身或其他循环语句，就称为循环的“嵌套”。**for 循环或 while 循环之间可以相互嵌套。**
##### 循环控制（`break` 语句）
在循环结构中，可以用 break 语句跳出当前循环体，从而中断当前循环。
#### 2.8 自定义函数 
一般格式为：
```
定义 def 函数名(参数):
    语句或语句组
    return 返回值
```
调用：
`函数名(参数)`

?> 参数是用来向函数传递值的，可以省略；参数也可以有多个，中间用`,`分割，调用时要注意参数顺序；另外return 语句将值返回给调用者，如果没有返回值，该语句可以省略。

例如：
```Python
def f(a,b):
    c=a**2+b
    return c
print(f(10,2))
#自定义函数 f 的作用是计算并返回`a**2+b`的值，当语句`f(10,2)`调用函数 f 时，10 和2 分别作为两个参数值依次传递给 a 和 b，所以程序输出 102。如果第 4 行改成`print(f(2,10))`，交换参数顺序，程序将输出 14。
```
输出：
```Python(IDLE)
102
```

_End._
