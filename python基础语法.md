# 1、变量与数据类型

## 一、注释

### 1. 注释的作用

> - 通过用自己熟悉的语言，在程序中对某些代码进行标注说明，这就是注释的作用，能够大大增强程序的可读性。

### 2. 注释的分类及语法

注释分为两类：==单行注释== 和 ==多行注释==。

- 单行注释

```python
# 注释内容
```

- 多行注释

```python
"""
	第一行注释
	第二行注释
"""
'''
	注释1
	注释2
'''
```

> 快捷键： ==ctrl + /==

#### 2.1 快速体验

- 单行注释

``` python
# 输出hello world
print('hello world')

print('hello Python')  # 输出(简单的说明可以放到一行代码的后面，一般习惯代码后面添加两个空格再书写注释文字)
```

- 多行注释

``` python
"""
    下面输出的作用，输出内容分别是：
    hello Python
"""
print('hello Python')

'''
    下面输出的作用，输出内容分别是：
    hello Python
'''
print('hello Python')
```

> 注意：解释器不执行任何的注释内容。

### 总结

- 注释的作用

用人类熟悉的语言对代码进行解释说明，方便后期维护。

- 注释的分类
  - 单行： `# 注释内容`，快捷键ctrl+/
  - 多行：`""" 注释内容 """` 或 `''' 注释内容 '''`
- 解释器不执行注释内容



## 二、变量

### 1.  变量的作用

程序中，数据都是临时存储在内存中，为了更快速的查找或使用这个数据，通常我们把这个数据在内存中存储之后定义一个名称，这个名称就是变量。

![image-20190122123202213](C:/Users/谷建豪/Desktop/Python核心编程/课件/01-Python基础入门/05-变量.assets/image-20190122123202213.png)

> 变量就是一个存储数据的的时候当前数据所在的内存地址的名字而已。

### 2.  定义变量

```python
变量名 = 值
```

> 变量名自定义，要满足==标识符==命名规则。

#### 2.1  标识符

标识符命名规则是Python中定义各种名字的时候的统一规范，具体如下：

- 由数字、字母、下划线组成
- 不能数字开头
- 不能使用内置关键字
- 严格区分大小写

```html
False     None    True   and      as       assert   break     class  
continue  def     del    elif     else     except   finally   for
from      global  if     import   in       is       lambda    nonlocal
not       or      pass   raise    return   try      while     with  
yield
```

#### 2.2 命名习惯

- 见名知义。
- 大驼峰：即每个单词首字母都大写，例如：`MyName`。
- 小驼峰：第二个（含）以后的单词首字母大写，例如：`myName`。
- 下划线：例如：`my_name`。

#### 2.3 使用变量

``` python
# 定义变量：存储数据 计算机科学与技术
schoolName = '计算机科学与技术'
print(schoolName)

# 定义变量：存储数据TOM
my_name = 'TOM'
print(my_name)
```

#### 2.4 认识bug

所谓bug，就是程序中的错误。如果程序有错误，需要程序员排查问题，纠正错误。

![image-20210424111033147](C:\Users\谷建豪\AppData\Roaming\Typora\typora-user-images\image-20210424111033147.png)

### 3. Debug工具

Debug工具是PyCharm IDE中集成的用来调试程序的工具，在这里程序员可以查看程序的执行细节和流程或者调解bug。

Debug工具使用步骤：

1. 打断点
2. Debug调试

#### 3.1 打断点

- 断点位置

目标要调试的代码块的第一行代码即可，即一个断点即可。

- 打断点的方法

单击目标代码的行号右侧空白位置。

![image-20190115130541289](C:/Users/谷建豪/Desktop/Python核心编程/课件/01-Python基础入门/05-变量.assets/image-20190115130541289-7528741.png)

#### 3.2 Debug调试

打成功断点后，在文件内部任意位置 — 右键 -- Debug'文件名' — 即可调出Debug工具面板 -- 单击Step Over/F8，即可按步执行代码。

![image-20190115130809100](C:/Users/谷建豪/Desktop/Python核心编程/课件/01-Python基础入门/05-变量.assets/image-20190115130809100-7528889.png)

#### 3.2.1 Debug输出面板分类

- Debugger
  - 显示变量和变量的细节
- Console
  - 输出内容



### 4. 认识数据类型

**在 Python 里为了应对不同的业务需求，也把数据分为不同的类型。**

![image-20190111124628584](C:/Users/谷建豪/Desktop/Python核心编程/课件/01-Python基础入门/05-变量.assets/image-20190111124628584-7181988.png)

> 检测数据类型的方法：`type()`

```python
a = 1
print(type(a))  # <class 'int'> -- 整型

b = 1.1
print(type(b))  # <class 'float'> -- 浮点型

c = True
print(type(c))  # <class 'bool'> -- 布尔型

d = '12345'
print(type(d))  # <class 'str'> -- 字符串

e = [10, 20, 30]
print(type(e))  # <class 'list'> -- 列表

f = (10, 20, 30)
print(type(f))  # <class 'tuple'> -- 元组

h = {10, 20, 30}
print(type(h))  # <class 'set'> -- 集合

g = {'name': 'TOM', 'age': 20}
print(type(g))  # <class 'dict'> -- 字典
```

### 总结

- 定义变量的语法

``` python
变量名 = 值
```

- 标识符
  - 由数字、字母、下划线组成
  - 不能数字开头
  - 不能使用内置关键字
  - 严格区分大小写
- 数据类型
  - 整型：int
  - 浮点型：float
  - 字符串：str
  - 布尔型：bool
  - 元组：tuple
  - 集合：set
  - 字典：dict

## 三、输出

作用：程序输出内容给用户

```python
print('hello Python')

age = 18
print(age)

# 需求：输出“今年我的年龄是18岁”
```

### 一.  格式化输出

所谓的格式化输出即按照一定的格式输出内容。

#### 1.1 格式化符号

| 格式符号 |          转换          |
| :------: | :--------------------: |
|    %s    |         字符串         |
|    %d    |   有符号的十进制整数   |
|    %f    |         浮点数         |
|    %c    |          字符          |
|    %u    |    无符号十进制整数    |
|    %o    |       八进制整数       |
|    %x    | 十六进制整数（小写ox） |
|    %X    | 十六进制整数（大写OX） |
|    %e    | 科学计数法（小写'e'）  |
|    %E    | 科学计数法（大写'E'）  |
|    %g    |      %f和%e的简写      |
|    %G    |      %f和%E的简写      |

> 技巧

- %06d，表示输出的整数显示位数，不足以0补全，超出当前位数则原样输出
- %.2f，表示小数点后显示的小数位数。

#### 1.2 体验

格式化字符串除了%s，还可以写为`f'{表达式}'`

```python
age = 18 
name = 'TOM'
weight = 75.5
student_id = 1

# 我的名字是TOM
print('我的名字是%s' % name)

# 我的学号是0001
print('我的学号是%4d' % student_id)

# 我的体重是75.50公斤
print('我的体重是%.2f公斤' % weight)

# 我的名字是TOM，今年18岁了
print('我的名字是%s，今年%d岁了' % (name, age))

# 我的名字是TOM，明年19岁了
print('我的名字是%s，明年%d岁了' % (name, age + 1))

# 我的名字是TOM，明年19岁了
print(f'我的名字是{name}, 明年{age + 1}岁了')
```

> f-格式化字符串是Python3.6中新增的格式化方法，该方法更简单易读。

#### 1.3 转义字符

- `\n`：换行。
- `\t`：制表符，一个tab键（4个空格）的距离。

#### 1.4 结束符

> 想一想，为什么两个print会换行输出？

```python
print('输出的内容', end="\n")
```

> 在Python中，print()， 默认自带`end="\n"`这个换行结束符，所以导致每两个`print`直接会换行展示，用户可以按需求更改结束符。

### 总结

- 格式化符号
  - %s：格式化输出字符串
  - %d：格式化输出整数
  - %f：格式化输出浮点数
- f-字符串
  - f'{表达式}'
- 转义字符
  - \n：换行
  - \t：制表符
- print结束符

``` python
print('内容', end="")
```

