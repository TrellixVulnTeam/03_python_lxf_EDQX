[TOC]

### Python基础

##### 数据类型

1. 整数

   > 1,-100
   >
   > 0xf500

2. 浮点数

   > 1.23
   >
   > 1.23e9

3. 字符串

   >"abc",'abc',"I'm OK"
   >
   >'\n, \t,\\'

4. 布尔值

   > True,False
   >
   > and,or,not

5. 空值

   > None，与0不同。

6. 变量

   > 大小写英文、数字和_
   >
   > 不能数字开头

##### 字符串与编码

###### 字符编码

- ASCII

  > 1 byte
  >
  > 127个字符，英文大小写，数字和一些符号

- Unicode

  > 2个byte（常用）
  >
  > 包含ASCII

- UTF-8[^Note]

  > 1~6 byte，变长编码
  >
  > 常用字母 1 byte
  >
  > 常用汉字 3 byte
  >
  > 包含ASCII

  [^Note]: 计算机内存统一**Unicode**编码，存储或传输__UTF-8__编码

###### Python字符串

- Python3中，字符使用Unicode编码。

  ```
  >>> ord('A')
  65
  >>> ord('中')
  20013
  >>> chr(66)
  'B'
  >>> chr(25991)
  '文'
  ```

  如果知道字符的整数编码，还可以用十六进制这么写`str`：

  ```
  >>> '\u4e2d\u6587'
  '中文'
  ```


- Bytes类型数据

  ```
  x = b'ABC
  ```

  为了避免乱码问题，应当始终坚持使用UTF-8编码对`str`和`bytes`进行转换。

  ```
  #!/usr/bin/env python3
  # -*- coding: utf-8 -*-
  ```

- 格式化

  ```
  >>> 'Hello, %s' % 'world'
  'Hello, world'
  >>> 'Hi, %s, you have $%d.' % ('Michael', 1000000)
  'Hi, Michael, you have $1000000.'
  ```

##### 使用列表list和元组tuple

- list=[]

  1. 追加append

     ```
     >>> classmates.append('Adam')
     >>> classmates
     ['Michael', 'Bob', 'Tracy', 'Adam']
     ```

  2. 插入insert

     ```
     >>> classmates.insert(1, 'Jack')
     >>> classmates
     ['Michael', 'Jack', 'Bob', 'Tracy', 'Adam']
     ```

  3. 删除delete

     ```
     >>> classmates.pop()
     'Adam'
     >>> classmates
     ['Michael', 'Jack', 'Bob', 'Tracy']
     ```

- tuple=()

  - __不可变__

##### 使用字典dict和集合set

- dict={}

  1. 键值存储

     ```
     >>> d = {'Michael': 95, 'Bob': 75, 'Tracy': 85}
     >>> d['Michael']
     95
     ```

  2. 删除delete

     ```
     >>> d.pop('Bob')
     75
     >>> d
     {'Michael': 95, 'Tracy': 85}
     ```

- set={}

  1. add(key)

     ```
     >>> s.add(4)
     >>> s
     {1, 2, 3, 4}
     >>> s.add(4)
     >>> s
     {1, 2, 3, 4}
     ```

  2. remove(key)

     ```
     >>> s.remove(4)
     >>> s
     {1, 2, 3}
     ```

##### 函数

###### 内置函数

###### 定义函数

```
def my_abs(x):
    if x >= 0:
        return x
    else:
        return -x
```

###### 递归函数

```
def fact(n):
    if n==1:
        return 1
    return n * fact(n - 1)
```

##### 高级特性

###### 切片

```
>>> L[0:3]
['Michael', 'Sarah', 'Tracy']
```

###### 迭代

在Python中，迭代是通过`for ... in`来完成

###### 列表生成器

```
>>> [x * x for x in range(1, 11)]
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

###### 生成器 

```
>>> L = [x * x for x in range(10)]
>>> L
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
>>> g = (x * x for x in range(10))
>>> g
<generator object <genexpr> at 0x1022ef630>
```

###### 迭代器

##### 函数式编程

###### 高阶函数

1. 变成指向函数

   ```
   >>> f = abs
   >>> f(-10)
   10
   ```

2. 传入函数

   ```
   def add(x, y, f):
       return f(x) + f(y)
   ```

3. **map / reduce**

4. filter

5. sorted 排序算法

###### 返回函数

###### 匿名函数

###### 装饰器

###### 偏函数

##### 模块  

![1544882412826](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1544882412826.png)

###### 实用模块

1. 内建模块 

   ```
   import sys
   ```

2. 安装第三方模块

   - pip
   - Anaconda

##### 面向对象编程

###### 类和实例











