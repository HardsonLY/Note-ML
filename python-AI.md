[图片本地路径](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images)

# 一、Python基础

## 1. 基本语法元素

![image-20230222091921263](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102105374.png)



---

### 1.1 数据类型

#### 1.1.1 基本类型：数字、字符串、布尔

1. 数字

   ​		int 整型---整数

   ​		float 浮点型---带小数的数

   ​		complex 复数---a+bj

2. 字符串

   ```python
   "python123asdf"
   ```

3. 布尔类型

   ```python
   y = 2 > 1
   print(y)
   ```

#### 1.1.2 组合类型：列表、元组、字典、集合

1. 列表

   ```python
   list1 = [1, 2, 3, 4]
   print(list1[0]) # 1
   list1[0] = 7
   print(list1[0]) # 7
   ```

   列表中的元素可以进行修改

2. 元组

   ```python
   tuple1 = (1, 2, 3, 5)
   ```

   元组中的元素不支持修改

3. 字典

   通过“键：值” 的映射实现数据存储和查找

   ```python
   dict1 = {key1 : value1, key2 : value2, ...}
   student = {2001: "小明", 2002: "小张", 2003: "小红"}
   print(student[2002])
   ```

   字典是无序的

4. 集合

   一系列互不相等元素的集合，内部也是无序的

   ```python
   student_set = {"小红", "小张", "小明", "小红"}
   print(student_set) # {"小张", "小红", "小明"}
   ```

   

---

### 1.2 变量

#### 1.2.1 变量的概念

实实在在的对象：如数据、抽象

可变性：增删改查等

变量定义二要素：变量名、赋值

```python
x = 1
```

#### 1.2.2 变量的命名

![image-20230222154840152](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102105905.png)

- 可以用来做变量名

  - 大写字母、小写字母、数字、下划线、汉字及其组合
  - 严格区分大小写

- 不可以用来做变量名

  - 首字符不允许是数字

  - 变量名中间不能有空格

  - 不能与33个python保留字相同

    ![image-20230222094931161](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102105388.png)

#### 1.2.3 变量名定义技巧

- 变量名尽可能有实际意义，表征数据的某种特性

  ```python
  age_of_student = [13, 14, 17]
  ```

- 下划线（推荐：变量名和函数名）变量名由多个单词组成，用_连接多个单词

  ```python
  age_of_student = [13, 14, 17]
  ```

- 驼峰体（推荐：类名）变量名由多个单词组成，单词首字母大写

  ```python
  AgeOfStudent
  ```

- 尽量避免用中文和拼音作变量名

- 特殊的变量：常量（Π、e）变量名所有字母均为大写

  ```python
  MAX_ITERATION = 1000
  ```

#### 1.2.4 变量的赋值

1. 一般赋值

   通过等号自右向左进行赋值

   ```python
   x = 1 + 2
   ```

2. 增量赋值

   ```python
   x = 10
   x = x + 10
   x += 10
   ```

3. 打包赋值

   ```python
   x, y = 1, 2
   print(x, y) # 1, 2
   x, y = y, x
   print(x, y) # 2, 1
   ```



---

### 1.3 控制流程

#### 1.3.1 顺序流程

自顶向下依次执行

```python
# 实现1-5的整数求和
res = 0
res += 1
res += 2
res += 3
res += 4
res += 5
print(res)
```

#### 1.3.2 循环流程——遍历循环（for）

从可迭代对象中，一次取出每一个元素，并进行相应的操作

```python
# 实现1-5的整数求和
res = 0
for i in [1, 2, 3, 4, 5]:
    res += i
print(res)
```

#### 1.3.3 循环流程——无限循环（while）

```python
# 实现1-5的整数求和
res = 0
i = 0
while i <= 5:
    res += i
    i += 1
print(res)
```

#### 1.3.4 分支流程（if）

```python
age = 18
if age > 22:
    print("age > 22")
else:
    print("age < 22")
```



---

### 1.4 输入输出

#### 1.4.1 数据从哪里来

1. 外部文件导入
   - 从本地硬盘、网络端读入
   - 该部分在【文件、异常和模块】

2. 程序中定义

   ```python
   age = 18
   ```

3. 动态交互输入input

   ```python
   x = input("请输入一个数字：")
   print(type(x)) # str
   print(x)
   ```

4. eval()去掉引号

   ```python
   x = eval(input("请输入一个数字"))
   print(type(x)) # int
   print(x)
   ```

#### 1.4.2 数据到哪里去

1. 存储到本地硬盘或网络断端

   - 该部分在【文件、异常和模块】

2. 打印输出 print

   - 直接打印数据

     ```python
     print("dasfdsgdg ")
     ```

   - 打印变量

     ```python
     x = 124
     print(x)
     ```

   - 简单的组合打印

     ```python
     PI = 3.14
     E = 2.71
     print("PI = ", PI, "E = ", E)
     ```

     

   - print 默认换行

   - 换行控制 end=

     ```python
     print(123, end = "留在这里")
     print(345) # 123留在这里345
     ```

3. 格式化输出方法 format

   - 基本格式："字符{0}字符{1}字符".format(v0, v1)

     ```python
     PI = 3.14
     E = 2.71
     print("PI = {0}, E = {1}".format(PI, E)) # PI = 3.14, E = 2.71
     print("PI = {0}, E = {0}".format(PI, E)) # PI = 3.14, E = 3.14
     print("PI = {1}, E = {0}".format(PI, E)) # PI = 2.71, E = 3.14
     ```

   - 填充输出

     ```python
     # _____3.1415926535_______ 进行填充
     PI = 3.1415926535
     print("{0:_^20}".format(PI)) # ____3.1415926535____
     print("{0:*<30}".format(PI)) #3.1415926535******************
     ```

   - 数字千分位分隔符

     ```python
     print("{0:,}".format(100000000)) # 100,000,000
     print("{0:&>20,}".format(100000000)) # &&&&&&&&&100,000,000
     ```

   - 浮点数简化输出

     - 留两位小数

       ```python
       PI = 3.1415926535
       print("{0:.2f}".format(PI)) # 3.14
       ```

     - 按百分数输出

       ```python
       print("{0:.1%}".format(0.8979671256)) # 89.8%
       ```

     - 科学计数法输出

       ```python
       print("{0:.2e}".format(0.897189625)) # 8.97e-01
       ```

   - 整数的进制转换输出

     十进制整数转二进制、Unicode编码、十进制、八进制、十六进制输出

     ```python
     print("二进制{0:b}, Unicode码{0:c}, 十进制{0:d}, 八进制{0:o}, 十六进制{0:x}".format(450)) 
     # 二进制111000010, Unicode码ǂ, 十进制450, 八进制702, 十六进制1c2
     ```

   ![image-20230222153622559](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102105409.png)



---

### 1.5 程序格式

1. 行最大长度

   所有行限制的最大字符数为79

2. 缩进

   - 用缩进来表示语句间的逻辑
   - 在 for while if def class等: 之后下一行开始进行缩进，表明后续代码与前句之间的从属关系
   - 缩进量：4字符

3. 使用空格

   - 二元运算符两边加一个空格

     ```python
     x = 2
     y > 3
     x += 4
     ```

   - 使用不同优先级的运算符，考虑在最低优先级的运算符周围添加空格

     ```python
     x = x*2 - 1
     y = (a+b) * (a-b)
     ```

   - 在逗号后使用空格

   - 不要使用一个以上的空格

4. 避免使用空格

   在制定关键字参数或者默认参数值的时候，不要在 = 附近加空格

   ```python
   def fun(n=1, m=2):
       print(n, m)
   ```

5. 注释

   - 单行注释

     ```python
     x = 1 # 这是注释
     ```

   - 多行注释

     ```python
     """
     safhuidosf
     fsdfgdsg
     qwyfh
     """
     ```



## 2. 基本数据类型

![image-20230222155032316](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102105518.png)



---

### 2.1 数字类型

![image-20230305100243421](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102105337.png)

#### 2.1.1 数字类型的组成

1. 整数——不同进制的转换

   - 默认输入十进制

   - 二进制0b，八进制0o，十六进制0x

   - 十进制与其他进制的转换

     ```python
     a = bin(16) # 转二进制
     b = oct(16) # 转八进制
     c = hex(16) # 转十六进制
     print(a, b, c) # 0b10000 0o20 0x10
     ```

     注意：上述转换后的结果为字符串类型

   - 其他进制转十进制

     ```python
     d = int(a, 2) #二进制转十进制
     e = int(b, 8) # 八进制转十进制
     f = int(c, 16) # 十六进制转十进制
     print(d, e, f) # 16 16 16
     ```

2. 浮点数——不确定性

   不确定小数问题

   ```python
   print(0.1 + 0.2) # 0.30000000000000004
   ```

   计算机采用二进制的小数部分来表示浮点数的小数部分

   - 部分小数不能用二进制小数完全表示

     ![image-20230222161906741](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102105513.png)

   - 通常情况下不会影响计算精度

   - 四舍五入获得精确解

     ```python
     a = 3 * 0.1
     print(a) # 0.30000000000000004
     b = round(a, 1)
     print(b) # 0.3
     print(b == 0.3) # True
     ```

3. 复数——a + bj

   - 大写 J 或者 小写 j 均可
   - 虚部系数为1时，需要显式写出

#### 2.1.2 数字运算操作符（a 操作符 b）

1. 加减乘除运算：+, -. *, /

2. 取反： -

   ```python
   x = 1
   print(-x)
   ```

3. 乘方运算：**

   ```python
   2 ** 3
   ```

4. 整数商// 和 模运算%

   ```python
   13 // 5 # 整数商，x/y 向下取整
   13 % 5 # ，模运算，余数 13 = 2*5 + 3
   ```

**几点说明**：

- 整数与浮点数的运算结果是浮点数
- 除法运算的结果是浮点数

#### 2.1.3 数字运算操作函数

1. 求绝对值 abs()

   ```python
   abs(-5)
   ```

2. 幂次方 pow(x, n)

   ```python
   pow(2, 5) # 2^5
   print(pow(2, 5, 3)) # 2^5 % 3
   ```

3. 四舍五入 round(x, n)

   ```python
   a = 21.4326
   print(round(a)) # 默认四舍五入为整数
   print(round(a, 2)) # 参数2表示四舍五入后保留2位小数
   print(round(a, 5)) # 位数不足，无需补齐
   ```

4. 整数商和模运算 divmod(x, y)

   等价于返回二元元组（x // y, x % y）

   ```python
   print(divmod(13, 5)) # (2, 3)
   ```

5. 序列最大/ 最小值 max(), min()

   ```python
   a = [1, 34, 5, 7,898, 745, 23]
   print(max(a))
   print(min(a))
   ```

6. 求和 sum(x)

   ```python
   print(sum([1, 2, 3, 4, 5]))
   ```

7. 借助科学计算库 math / scipy / numpy

   ```python
   import math
   print(math.exp(1)) # 指数运算 e^1
   print(math.log2(2)) # 对数运算
   print(math.sqrt(4)) # 开平方运算
   
   import numpy as np
   a = [1, 2, 3, 4, 5]
   print(np.mean(a)) # 求均值
   print(np.median(a)) # 求中位数
   print(np.std(a)) # 求标准差
   ```



---

### 2.2 字符串类型

![image-20230305100318684](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102106466.png)

#### 2.2.1 字符串的表达

- 用 "" 或 '' 括起来的任意字符

- 字符串中有双引号或单引号的情况

  - 双中有单

  - 单中有双

  - 双中有双、单中有单——转义符 \

    ```python
    print("\"python"\ is good")
    ```

  - 转义符可以用来换行继续输入

#### 2.2.2 字符串的性质

1. 字符串的索引

   ```python
   s = "My name is Paper Pig"
   
   # 正向索引，从0开始
   print(s[0])
   print(s[3])
   print(s[4])
   
   # 反向索引，从-1开始
   print(s[-1])
   print(s[-2])
   ```

2. 字符串的切片

   > 变量名[开始位置：结束位置：切片间隔]

   - 切片间隔如不设置默认为1，可省略
   - 切片范围不包含结束位置
   - 起始位置是0时，可以省略
   - 结束位置省略，代表可以取到最后一个字符
   - 可以使用反向索引号

   ```python
   var = "python"
   print(var[0: -1: 2]) # pto
   ```

   - 反向切片

     - 起始位置时-1也可以省略
     - 结束位置省略，代表可以取到第一个字符

     ```python
     var = "python"
     print(var[:: -1]) # nohtyp
     ```

#### 2.2.3 字符串操作符

1. 字符串的拼接

   > 字符串1+字符串2

2. 字符串的成倍复制

   > 字符串 * n  n * 字符串

   ```python
   var = "python"
   print(var * 3) # pythonpythonpython
   print(3 * var) # pythonpythonpython
   ```

3. 成员运算

   - 子集 in 全集：任何一个连续的切片都是原字符串的子集

     ```python
     address = "Peter, John and Mike"
     print("Peter" in address) # True
     ```

   - 遍历字符串字符

     ```python
     for s in "address":
         print(s)
     ```

#### 2.2.4 字符串处理函数

1. 字符串的长度

   ```python
   s = "python"
   print(len(s))
   ```

2. 字符编码

   - 将中文字库、英文字母、数字、特殊字符等转换成计算机可识别的二进制数

     - 每个单一字符对应一个唯一的互不重复的二进制编码
     - Python中使用的是Unicode编码

   - 将字符转换为Unicode编码——ord(字符)

     ```python
     print(ord('l')) # 108
     ```

   - 将Unicode编码转换为字符——chr(Unicode编码)

     ```python
     print(chr(108)) # l
     ```

#### 2.2.5 字符串的处理方法

1. 字符串的分割——split

   - 返回一个列表
   - 原字符串不变

   ```python
   languages = "Java, C, C++, Python"
   print(languages.split(",")) # ['Java', ' C', ' C++', ' Python']
   ```

2. 字符串的聚合——“聚合字符”.join(可迭代数据类型)

   - 可迭代类型，如：字符串、列表

     ```python
     s = "12345"
     s_join = ",".join(s)
     print(s_join) # 1,2,3,4,5
     ```

   - 序列类型的元素必须是字符类型

     ```python
     s = ["1", "2", "3", "4", "5"]
     print("*".join(s)) # 1*2*3*4*5
     ```

3. 删除两端特定字符——字符串.strip(删除字符)

   - strip从两侧开始搜索，遇到指定字符执行删除，遇到非指定字符，搜索停止
   - 类似的还有做删除lstrip和右删除rstrip

   ```python
   s = "             I have many blanks         "
   print(s.strip(" ")) # I have many blanks
   print(s.lstrip(" ")) # I have many blanks         
   print(s.rstrip(" ")) #              I have many blanks
   ```

4. 字符串的替换——字符串.replace("被替换", "替换成")

   ```python
   s = "Python is coming"
   s1 = s.replace("Python", "Py")
   print(s1) # Py is coming
   print(s) # Python is coming
   ```

5. 字符串统计——字符串.count("待统计字符串")

   ```python
   s = "xasdgwuqyfgasxasasasasasasasfxxxxxxxc"
   print(s.count("x")) # 9
   print(s.count("sa")) # 6
   ```

6. 字符串字母大小写

   ```python
   s = "pYtHon"
   print(s.upper()) # PYTHON 字母全部大写
   print(s.lower()) # python 字母全部小写
   print(s.title()) # Python 首字母大写
   ```



---

### 2.3 布尔类型

![image-20230305100347291](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102106312.png)

#### 2.3.1 逻辑运算的结果

```python
a = 10
print(a > 8) # True
print(a == 10) # True
print(a < 10) # False
```

- any(), all()

  ```python
  print(any([False, 1, 0, None])) # 只要有非0 就为True
  print(all([False, 1, 0, None])) # 全都是非0，才能True
  ```

#### 2.3.2 指示条件

```python
n = 2800
while True:
    m = eval(input("请输入一个正整数"))
    if m == n:
        print("猜对了")
        break
    elif m > n:
        print("太大了")
    else:
        print("太小了")
```

#### 2.3.3 作为掩码

```python
import numpy as np
x = np.array([1, 2, 4, 3, 6, 5]) #定义numpy数组
print(x > 3) # [False False  True False  True  True]
print(x[x > 3]) # [4 6 5]
```



---

### 2.4 类型判别及类型转换

![image-20230305100357986](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102106348.png)

#### 2.4.1 类型判别

- type(变量)

  ```python
  age = 20
  name = "Mike"
  print(type(age)) # <class 'int'>
  print(type(name)) # <class 'str'>
  ```

- isinstance(变量, 预判类型)：**承认继承**

- 变量类型是预判类型的子类型，则为真，否则为假

  ```python
  age = 20
  name = "Mike"
  
  print(isinstance(age, int)) # True
  print(isinstance(age, object)) # True
  print(isinstance(name, object)) # True
  ```

- 字符串检查方法

  - 字符串.isdigit() 字符串是否只有数字组成

    ```python
    age = "20"
    name = "324khdfoas"
    print(age.isdigit()) # True
    print(name.isdigit()) # False
    ```

  - 字符串.isalpha()字符串是否只有字母组成

    ```python
    age = "20"
    name = "324khdfoas"
    txt = "dfsjihgg"
    print(name.isalpha()) # False
    print(txt.isalpha()) # True
    ```

  - 字符串.isalnum()字符串是否只有数字和字母组成

    ```python
    age = "20"
    name = "324khdfoas"
    txt = "dfsjihgg"
    address = "dashdiu1344&&&"
    
    print(name.isalnum()) # True
    print(txt.isalnum()) # True
    print(age.isalnum()) # True
    print(address.isalnum()) # False
    ```

#### 2.4.2 类型转换

- 数字类型转字符串——str(数字类型)

  ```python
  age = 20
  print("My age is " + str(age))
  ```

- 仅有数字组成的字符串转数字——int()，float()，evail()

  ```python
  s1 = "20"
  s2 = "213.4"
  
  print(int(s1)) # 20
  print(float(s2)) # 213.4
  print(float(s1)) # 20.0
  
  print(eval(s1)) # 20
  print(eval(s2)) # 213.4
  ```



## 3. 组合数据类型

![image-20230305100724909](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102106436.png)



---

### 3.1 列表

![image-20230308155313596](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102106571.png)

#### 3.1.1 列表的表达

- 序列类型：内部元素有位置关系，能通过位置序号访问其中元素

- 列表是一个可以使用多种类型元素，支持元素的增删改查操作的序列类型

  ```python
  ls = ["Python", 1989, True, {"Version": 3.7}]
  print(ls) # ['Python', 1989, True, {'Version': 3.7}]
  ```

- 另一种产生方式：list(可迭代对象)

- 可迭代对象包括：字符串、元组、集合、range()等

  - 字符串转列表

    ```python
    print(list("人工智能是未来的趋势")) # ['人', '工', '智', '能', '是', '未', '来', '的', '趋', '势']
    ```

  - 元组转列表

    ```python
    print(list(("我", "们", "很", "像"))) # ['我', '们', '很', '像']
    ```

  - 集合转列表

    ```python
    print(list({"李雷", "韩梅梅", "Jina", "Green"})) # ['李雷', 'Green', '韩梅梅', 'Jina']
    ```

  - 特殊的range()

    ```python
    for i in [0, 1, 2, 3, 4, 5]:
        print(i)
    
    for i in range(6):
        print(i)
    ```

    - range(起始数字，终止数字，数字间隔)

    - 如果起始数字缺省，默认为0

    - 不可以缺少终止数字，终止数字取不到

    - 数字间隔缺省，默认为1

      ```python
      for i in range(1, 11, 2):
          print(i)
      ```

  - range()转列表

    ```python
    print(list(range(1, 11, 2))) # [1, 3, 5, 7, 9]
    ```

#### 3.1.2 列表的性质

- 列表的长度——len(列表)

  ```python
  ls = [1, 2, 3, 4, 5]
  print(len(ls)) # 5
  ```

- 列表的索引——与同为序列类型的字符串完全相同

  变量名[位置编号]

  - 正向索引从0开始
  - 反向索引从-1开始

  ```python
  cars = ["BYD", "BMW", "AUDI", "TOYOTA"]
  print(cars[0])
  print(cars[-1])
  ```

- 列表的切片

  变量名[开始位置: 结束位置: 切片间隔]

  - 正向切片

    ```python
    cars = ["BYD", "BMW", "AUDI", "TOYOTA"]
    
    # 前三个元素，开始位置缺省，默认为0，切片间隔缺省，默认为1
    print(cars[:3]) # ['BYD', 'BMW', 'AUDI']
    
    # 第二个到第四个元素，前后索引差为2
    print(cars[1:4:2]) # ['BMW', 'TOYOTA']
    
    # 获取整个列表，结束位置缺省，默认取值到最后
    print(cars[:]) # ['BYD', 'BMW', 'AUDI', 'TOYOTA']
    
    # 获取前两个元素
    print(cars[-4:-2]) # ['BYD', 'BMW']
    ```

  - 反向切片

    ```python
    cars = ["BYD", "BMW", "AUDI", "TOYOTA"]
    
    # 开始位置缺省,默认为-1
    print(cars[:-4:-1]) # ['TOYOTA', 'AUDI', 'BMW']
    
    # 获取反向列表
    print(cars[::-1]) # ['TOYOTA', 'AUDI', 'BMW', 'BYD']
    ```

#### 3.1.3 列表的操作符

- 用 list1 + list2 的形式实现列表的拼接

  ```python
  a = [1, 2, 5]
  b = [3, 4, 3]
  print(a + b) # [1, 2, 5, 3, 4, 3]
  ```

- 用 n * list 或者 list * n 实现列表的成倍复制

  初始化列表的一种方式

  ```python
  print([0] * 10) # [0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
  ```

#### 3.1.4 列表的操作方法

1. 增加元素

   - 在末尾增加元素——列表.append(待增元素)

     ```python
     languages = ["Python", "Java", "C++"]
     languages.append("R")
     print(languages) # ['Python', 'Java', 'C++', 'R']
     ```

   - 在任意位置插入元素——列表.insert(位置编号，待增元素)

     在位置编号相应元素前插入待增元素

     ```python
     languages = ["Python", "Java", "C++"]
     languages.insert(1, "C")
     print(languages) # ['Python', 'C', 'Java', 'C++']
     ```

   - 在末尾整体并入另一列表——列表1.extend(列表2)

     - append将列表2整体作为一个元素添加到列表1中

       ```python
       languages = ["Python", "Java", "C++"]
       languages.append(["Ruby", "PHP"])
       print(languages) # ['Python', 'Java', 'C++', ['Ruby', 'PHP']]
       ```

     - extend将列表2内的元素诸葛添加到列表1中

       ```python
       languages = ["Python", "Java", "C++"]
       languages.extend(["Ruby", "PHP"])
       print(languages) # ['Python', 'Java', 'C++', 'Ruby', 'PHP']
       ```

2. 删除元素

   - 删除列表i位置的元素——列表.pop(位置)

     ```python
     languages = ['Python', 'Java', 'C++', 'Ruby', 'PHP']
     languages.pop(1)
     print(languages) # ['Python', 'C++', 'Ruby', 'PHP']
     ```

   - 不写位置信息，默认删除最后一个元素

     ```python
     languages = ['Python', 'Java', 'C++', 'Ruby', 'PHP']
     languages.pop()
     print(languages) # ['Python', 'Java', 'C++', 'Ruby']
     ```

   - 删除列表中第一次出现的待删元素——列表.remove(待删元素)

     ```python
     languages = ['Python', 'Java', 'C++', 'Ruby', 'PHP', 'C++']
     languages.remove("C++")
     print(languages) # ['Python', 'Java', 'Ruby', 'PHP', 'C++']
     ```

3. 查找元素

   - 列表中第一次出现待查元素的位置——列表.index(待查元素)

     ```python
     languages = ['Python', 'C', 'C++', 'R', 'Java']
     index = languages.index("R")
     print(index) # 3
     ```

4. 修改元素

   ```python
   languages = ['Python', 'C', 'C++', 'R', 'Java']
   languages[2] = "PyTorch"
   print(languages) # ['Python', 'C', 'PyTorch', 'R', 'Java']
   ```

5. 列表的复制

   - 错误方式

     ```python
     languages = ['Python', 'C', 'C++', 'R', 'Java']
     languages_2 = languages
     print(languages_2) # ['Python', 'C', 'C++', 'R', 'Java']
     print(languages) # ['Python', 'C', 'C++', 'R', 'Java']
     print("---------------------")
     languages.pop()
     print(languages) # ['Python', 'C', 'C++', 'R']
     print(languages_2) # ['Python', 'C', 'C++', 'R']
     ```

   - 正确方式——浅拷贝

     - 列表.copy()

       ```python
       languages = ['Python', 'C', 'C++', 'R', 'Java']
       languages_2 = languages.copy()
       print(languages_2) # ['Python', 'C', 'C++', 'R', 'Java']
       languages.pop()
       print(languages_2) # ['Python', 'C', 'C++', 'R', 'Java']
       ```

     - 列表[:]

       ```python
       languages = ['Python', 'C', 'C++', 'R', 'Java']
       languages_2 = languages[:]
       print(languages_2) # ['Python', 'C', 'C++', 'R', 'Java']
       languages.pop()
       print(languages_2) # ['Python', 'C', 'C++', 'R', 'Java']
       ```

6. 列表的排序

   - 使用 列表.sort() 对列表进行永久排序

   - 直接在列表上进行操作，无返回值

     ```python
     ls = [2, 3, 1, 5, 4, 7, 5, 9, 8]
     ls.sort()
     print(ls)
     ```

   - 递减排列

     ```python
     ls = [2, 3, 1, 5, 4, 7, 5, 9, 8]
     ls.sort(reverse=True)
     print(ls) # [9, 8, 7, 5, 5, 4, 3, 2, 1]
     ```

   - 使用 sorted(列表) 对列表进行临时排序

   - 原列表保持不变，返回排序后的列表

     ```python
     ls = [2, 3, 1, 5, 4, 7, 5, 9, 8]
     ls_sort = sorted(ls)
     ls_sort_True = sorted(ls, reverse=True)
     print(ls) # [2, 3, 1, 5, 4, 7, 5, 9, 8]
     print(ls_sort) # [1, 2, 3, 4, 5, 5, 7, 8, 9]
     print(ls_sort_True) # [9, 8, 7, 5, 5, 4, 3, 2, 1]
     ```

7. 列表的翻转

   - 使用 列表.reverse() 对列表进行永久翻转

   - 直接在列表上进行操作，无返回值

     ```python
     ls = [2, 3, 1, 5, 4, 7, 5, 9, 8]
     print(ls) # [8, 9, 5, 7, 4, 5, 1, 3, 2]
     ```

     ```python
     ls = [2, 3, 1, 5, 4, 7, 5, 9, 8]
     print(ls[::-1] # [8, 9, 5, 7, 4, 5, 1, 3, 2]
     ```

8. 使用 for循环 对列表进行遍历

   ```python
   ls = [2, 3, 1, 5, 4, 7, 5, 9, 8]
   for i in ls:
       print(i)
   ```



---

### 3.2 元组

![image-20230308155345900](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102106481.png)

#### 3.2.1 元组的表达

元组是一个可以使用多种类型元素，一旦定义，内部元素不支持增、删、修改操作的序列类型

通俗的讲，可以将元组视作 **`不可变的列表`**

```python
names = ("Peter", "Mike", "John", "Marry")
```

#### 3.2.2 元组的操作

- 不支持元组增加、元素删除、元素修改操作
- 其他操作与列表的操作完全一致

#### 3.2.3 元组的常见用处

**打包和解包**

- 例1

  ```python
  # 实现 x 的平方和立方
  def f1(x):
      # 实现打包返回
      return x **2, x**3
  
  print(f1(3)) # (9, 27)
  print(type(f1(3))) # <class 'tuple'>
  
  # 实现解包赋值
  a, b = f1(3)
  print(a) # 9
  print(b) # 27
  ```

- 例2

  ```python
  numbers = [201901, 201902, 201903]
  name = ["小明", "小红", "小强"]
  list(zip(numbers, name))
  
  for number, name in zip(numbers, name):
      print(number, name)
  
  '''
  201901 小明
  201902 小红
  201903 小强
  '''
  ```



---

### 3.3 字典

![image-20230308155404022](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102106179.png)

#### 3.3.1 字典的表达

- 映射类型：通过 `“键”-“值”` 的映射实现数据存储和查找

- 常规的字典是无序的

  ```python
  students = {201901: '小明', 201902: '小红', 201903: '小强'}
  print(students) # {201901: '小明', 201902: '小红', 201903: '小强'}
  ```

- 字典键的要求
  1. 字典的键不能重复，有重复的话，后边的会把前边的覆盖掉
  2. 字典的键必须是不可变类型，如果键可变，就找不到对应存储的值了
     - `不可变类型`：数字、字符串、元组，一旦确定，他自己就是他自己，变了就不是他了
     - `可变类型`：列表、字典、集合。一旦确定，还可以随意增删改

#### 3.3.2 字典的性质

- 字典的长度——键值对的个数

  ```python
  students = {201901: '小明', 201902: '小红', 201903: '小强'}
  print(len(students)) # 3
  ```

- 字典的索引——通过 字典[键] 的形式来获取对应的值

  ```python
  students = {201901: '小明', 201902: '小红', 201903: '小强'}
  print(students[201902]) # 小红
  ```

#### 3.3.3 字典的操作方法

1. 增加键值对——变量名[新键] = 新值

   ```python
   students = {201901: '小明', 201902: '小红', 201903: '小强'}
   students[201904] = "小香"
   print(students) # {201901: '小明', 201902: '小红', 201903: '小强', 201904: '小香'}
   ```

2. 删除键值对

   - 通过 del 变量名[待删除键]

     ```python
     students = {201901: '小明', 201902: '小红', 201903: '小强'}
     del students[201903]
     print(students) # {201901: '小明', 201902: '小红'}
     ```

   - 通过 变量名.pop(待删除键)

     ```python
     students = {201901: '小明', 201902: '小红', 201903: '小强'}
     delete_value = students.pop(201903)
     print(delete_value) # 小强
     print(students) # {201901: '小明', 201902: '小红'}
     ```

   - 变量名.popitem() 随机删除一个键值对，并以元组返回删除键值对

     ```python
     students = {201901: '小明', 201902: '小红', 201903: '小强'}
     del_key, del_value = students.popitem()
     print(del_key, del_value)
     print(students)
     ```

3. 修改值

   通过先索引后赋值的方式对相应的值进行修改

   ```python
   students = {201901: '小明', 201902: '小红', 201903: '小强'}
   students[201902] = '小绿'
   print(students) # {201901: '小明', 201902: '小绿', 201903: '小强'}
   ```

4. d.get() 方法

   d.get(key, default) 从字典d中获取 键key 对应的值。如果没有这个键，则返回 default

   ```python
   # 统计 “牛奶奶找刘奶奶买牛奶” 中字符出现的频率
   s = "牛奶奶找刘奶奶买牛奶"
   d = {}
   for i in s:
       d[i] = d.get(i, 0) + 1
   print(d) # {'牛': 2, '奶': 5, '找': 1, '刘': 1, '买': 1}
   ```

5. d.keys() 和 d.value() 方法

   ```python
   students = {201901: '小明', 201902: '小红', 201903: '小强'}
   print(list(students.keys())) # [201901, 201902, 201903]
   print(list(students.values())) # ['小明', '小红', '小强']
   ```

6. d.items()方法 及 字典的遍历

   ```python
   students = {201901: '小明', 201902: '小红', 201903: '小强'}
   print(list(students.items()))
   for key, value in students.items():
       print(key, value)
   '''
   [(201901, '小明'), (201902, '小红'), (201903, '小强')]
   201901 小明
   201902 小红
   201903 小强
   '''
   ```



---

### 3.4 集合

![image-20230308155448628](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102106518.png)

#### 3.4.1 集合的表达

- 一系列互不相等的元素的无序集合
- 元素必须是不可变类型：数字、字符串或元组，可视作字典的键
- 可以看作是没有值，或者值为None的字典

```python
students = {"小明", "小红", "小强", "小明"}
print(students) # {'小明', '小强', '小红'}
```

#### 3.4.2 集合的运算

- 小例子：通过集合进行交集、并集的运算

  ```python
  Chinese_A = {"刘德华", "张学友", "张曼玉", "钟楚红", "古天乐", "林青霞"}
  Math_A = {"林青霞", "郭富城", "王祖贤", "刘德华", "张曼玉", "黎明"}
  
  # 数学和语文都为A
  print(Chinese_A & Math_A)
  
  # 数学和语文至少一门为A
  print(Chinese_A | Math_A)
  
  # 数学和语文只有一门为A
  print(Chinese_A ^ Math_A)
  
  # 语文A，但数学不是A
  print(Chinese_A - Math_A)
  
  # 数学A，但语文不是A
  print(Math_A - Chinese_A)
  
  '''
  {'刘德华', '林青霞', '张曼玉'}
  {'林青霞', '张曼玉', '黎明', '郭富城', '王祖贤', '刘德华', '钟楚红', '古天乐', '张学友'}
  {'黎明', '郭富城', '王祖贤', '钟楚红', '古天乐', '张学友'}
  {'钟楚红', '古天乐', '张学友'}
  {'王祖贤', '郭富城', '黎明'}
  '''
  ```

#### 3.4.3 集合的操作方法

- 增加元素——S.add(x)

  ```python
  stars = {"刘德华", "张学友", "张曼玉", "钟楚红", "古天乐"}
  print(stars) # {'古天乐', '张学友', '张曼玉', '刘德华', '钟楚红'}
  stars.add("林青霞")
  print(stars) # {'林青霞', '古天乐', '张学友', '张曼玉', '刘德华', '钟楚红'}
  ```

- 移除元素——S.remove(x)

  ```python
  stars = {"刘德华", "张学友", "张曼玉", "钟楚红", "古天乐"}
  print(stars) # {'张学友', '张曼玉', '钟楚红', '古天乐', '刘德华'}
  stars.remove("张曼玉")
  print(stars) # {'张学友', '钟楚红', '古天乐', '刘德华'}
  ```

- 集合的长度——len(S)

  ```python
  stars = {"刘德华", "张学友", "张曼玉", "钟楚红", "古天乐"}
  print(len(stars)) # 5
  ```

- 集合的遍历——借助for循环

  ```python
  stars = {"刘德华", "张学友", "张曼玉", "钟楚红", "古天乐"}
  for star in stars:
      print(star)
  '''
  古天乐
  张学友
  张曼玉
  刘德华
  钟楚红
  '''
  ```



## 4. 程序控制结构

![image-20230308160003427](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102106312.png)

非顺序式的程序控制，往往需要根据一定的条件，决定程序运行的路线。因此，我们首先认识一下什么叫做条件测试。

---

### 4.1 条件测试

![image-20230309172200031](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102106296.png)

##### 4.1.1 比较运算

```python
a = 10
b = 8
print(a > b)
print(a < b)
print(a >= b)
print(a <= b)
print(a == b)
print(a != b)
```

- 非空

  ```python
  ls = []
  if ls:
      print("非空")
  else:
      print("空的")
  ```

#### 4.1.2 逻辑运算

- 与、或、非

  ```py
  a = 10
  b = 8
  c = 12
  print((a > b) and (b > c))
  print((a > b) or (b > c))
  print(not (a > b))
  
  '''
  False
  True
  False
  '''
  ```

- 复合逻辑运算的优先级——非 > 与 > 或

  ```python
  print(True or True and False) # True
  print((True or True) and False) # False
  ```

#### 4.1.3 存在运算

```python
cars = ["BYD", "BMW", "AUDI", "TOYOTA"]

# 元素 in 列表/字符串
print("BMW" in cars)
print("BENZ" in cars)

# 元素 not in 列表/字符串
print("BMW" not in cars)
print("BENZ" not in cars)
```



---

### 4.2 分支结构——if语句

![image-20230309172233120](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102106152.png)

#### 4.2.1 单分支

略

#### 4.2.2 二分支

略

#### 4.2.3 多分支

略

#### 4.2.4 嵌套语句

题目：年满18周岁，在非公共场合可以抽烟。判断某种情形下是否可以抽烟

```python
age = eval(input("请输入年龄: "))
if age > 18:
    is_public_place = bool(eval(input("公共场合输入1，非公共场合输入0：")))
    if not is_public_place:
        print("可以抽烟")
    else:
        print("不可以抽烟")
else:
    print("未成年禁止抽烟")
```



---

### 4.3 遍历循环——for循环

![image-20230309172254200](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102106451.png)

```python
for 元素 in 可迭代对象:
    执行语句
```

- 执行过程——从可迭代对象中，一次取出每一个元素，并进行相应的操作

  1. 直接迭代——列表[]，元组()，集合{}，字符串""

     ```python
     graduates = ("李磊", "韩梅梅", "Jina")
     for graduate in graduates:
         print(graduate)
     ```

  2. 变换迭代——字典

     ```python
     students = {201901: "小芳", 201902: "霄宫", 201903: "小强"}
     for key, value in students.items():
         print(key, value)
     
     print("--------------------")
     for student in students:
         print(student)
     
     print("--------------------")
     for key in students.keys():
         print(key)
     
     print("--------------------")
     for value in students.values():
         print(value)
     
     '''
     201901 小芳
     201902 霄宫
     201903 小强
     --------------------
     201901
     201902
     201903
     --------------------
     201901
     201902
     201903
     --------------------
     小芳
     霄宫
     小强
     '''
     ```

  3. range()对象

     ```python
     res = []
     for i in range(10000):
         res.append(i ** 2)
     print(res[:5]) # 前五个元素
     print(res[-1]) # 最后一个元素
     
     print("--------------------")
     res = []
     for i in range(1, 10, 2):
         res.append(i ** 2)
     print(res)
     
     '''
     [0, 1, 4, 9, 16]
     99980001
     --------------------
     [1, 9, 25, 49, 81]
     '''
     ```

- 循环控制——break 和 continue

  - break结束整个循环
  - continue结束本次循环

- for 与 else 的配合

  如果for循环全部执行完毕，没有被break中止，则运行else块

  ```python
  # 1组产品的性能评分
  product_scores = [89, 90, 99, 76, 67, 78, 92, 85, 77, 82]
  # 如果低于75分的超过两个，则该组产品不合格
  i = 0
  for score in product_scores:
      if score < 75:
          i += 1
      if i == 2:
          print("产品抽检不合格")
          break
  else:
      print("产品抽检合格")
  ```



---

### 4.4 无限循环——while循环

![image-20230309172332288](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102106452.png)

#### 4.4.1 主要形式

```python
while 判断语句:
    执行语句
```

条件为真，执行语句

条件为假，while循环结束

```python
albert_age = 18
guess = int(input(">>: "))

while guess != albert_age:
    if guess > albert_age:
        print("猜的太大了")
    elif guess < albert_age:
        print("猜的太小了")
    guess = int(input(">>: "))
print("猜对了")
```

#### 4.4.2 while 与 风向标

```python
albert_age = 18
flag = True

while flag:
    guess = int(input(">>: "))
    if guess > albert_age:
        print("猜的太大了")
    elif guess < albert_age:
        print("猜的太小了")
    else:
        print("猜对了")
        flag = False
```

#### 4.4.3 while 与循环控制 break、continue

```python
albert_age = 18

while True:
    guess = int(input(">>: "))
    if guess > albert_age:
        print("猜的太大了")
    elif guess < albert_age:
        print("猜的太小了")
    else:
        print("猜对了")
        break
```

```python
i = 0
while i < 10:
    i += 1
    if i % 2 == 0:
        continue
    print(i)
```

#### 4.4.4 while 与 else

如果while循环全部执行完毕，没有被break中止，则运行else块

```python
count = 0
while count <= 5:
    count += 1
    print("Loop", count)
else:
    print("循环正常执行完毕")
```



---

### 4.5 控制语句注意问题

![image-20230309172356592](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303102107282.png)

1. 尽可能减少多层嵌套

   可读性差，容易把人搞疯

2. 避免死循环

   条件一直成立，循环永无止境

3. 封装过于复杂的判断条件

   如果条件判断的表达式过于复杂，出现了太多的 not、and、or等，导致可读性大打折扣

   可以考虑将条件封装为函数：

   ```python
   numbers = (10, 8, 6, 2, 0)
   a, b, c, d, e = numbers
   def judge(num):
       a, b, c, d, e = num
       x = a > b
       y = c > d
       z = not e
       return x and y and z
   
   if judge(numbers):
       print("hihdasidoh")
   ```



## 5. 函数——面向过程的编程

![image-20230313094657407](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303130946494.png)

---

### 5.1 函数的定义及调用

![image-20230313151956663](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303131519772.png)

#### 5.1.1 为什么要用函数

1. 提高代码的复用性——抽象出来，封装成函数
2. 将复杂的大问题分解成一系列小问题，分而治之——模块化设计的思想
3. 利于代码的维护和管理

```python
# 阶乘
def factoria(n):
    res = 1
    for i in range(1, n+1):
        res *= i
    return res

print(factoria(5))
print(factoria(20))
```

#### 5.1.2 函数的定义及调用

白箱子：输入——处理——输出

三要素：参数、函数体、返回值

1. 定义

   ```python
   # 求正方体的面积
   def area_of_square(length_of_side):
       square_area = pow(length_of_side, 2)
       return square_area
   ```

2. 调用

   ```python
   area = area_of_square(5)
   print(area)
   ```

#### 5.1.3 参数传递

1. 形参与实参

   - 形参（形式参数）
   - 实参（实际参数）

2. 参数位置

   - 严格按照位置顺序，用实参对形参进行赋值（关联）
   - 一般用在参数比较少的时候
   - 实参与形参个数必须一一对应，一个不多一个不少

3. 关键字参数

   - 打破位置限制，直呼其名的进行值的传递（形参 = 实参）

   - 必须遵守遵守实参与形参数量上的一一对应

   - 多用在参数比较多的场合

     ```python
     def function(x, y, z):
         print(x, y, z)
     
     function(y = 1, z = 2, x = 3)
     ```

   - 位置参数可以与关键字参数混合使用

   - 但是，位置参数必须放在关键字参数的前面

     ```python
     def function(x, y, z):
         print(x, y, z)
     
     function(3, z = 2, y = 1)
     ```

   - 不能为同一个形参重复传值

4. 默认参数

   - 在定义阶段就给形参赋值——该形参的常用值

   - 机器学习库中类的方法里比较常见

   - 调用函数时，可以不对该形参传值

     ```python
     def register(name, age, gender = "male"):
         print(name, age, gender)
     
     register("大眼仔", 19)
     ```

   - 也可以按正常的形参进行传值

     ```python
     def register(name, age, gender = "male"):
         print(name, age, gender)
     
     register("大眼仔", 19, "female")
     ```

   - 位置形参必须在默认形参的前面

   - 默认参数应该设置为不可变类型（数字、字符串、元组）

   - 让参数变成可选的

     ```python
     def name(first_name, last_name, middle_name = None):
         if middle_name:
             return first_name + middle_name + last_name
         else:
             return first_name + last_name
     print(name("大", "仔"))
     print(name("大", "仔", "眼"))
     ```

5. 可变长参数——*args

   - 不知道回传过来多少参数 *args

   - 该形参必须放在参数列表的最后

     ```python
     def foo(x, y, z, *args):
         print(x, y, z)
         print(args)
     
     foo(3, 4, 5, 6, 7, 7, 8)
     '''
     3 4 5
     (6, 7, 7, 8)
     '''
     ```

   - 实参打散

     ```python
     def foo_2(x, y, z, *args):
         print(x, y, z)
         print(args)
     
     foo_2(1, 2, 3, [4, 5, 6])
     foo_2(1, 2, 3, *[4, 5, 6])
     '''
     1 2 3
     ([4, 5, 6],)
     1 2 3
     (4, 5, 6)
     '''
     ```

6. 可变长参数——**kwargs

   ```python
   def foo_3(x, y, z, **kwargs):
       print(x, y, z)
       print(kwargs)
   foo_3(1, 2, 3, a = 4, b = 5, c = 6)
   '''
   1 2 3
   {'a': 4, 'b': 5, 'c': 6}
   '''
   ```

   - 字典实参打散

     ```python
     def foo_3(x, y, z, **kwargs):
         print(x, y, z)
         print(kwargs)
     foo_3(1, 2, 3, **{"a": 4, "b": 5, "c": 6})
     '''
     1 2 3
     {'a': 4, 'b': 5, 'c': 6}
     '''
     ```

   - 可变长参数的组合使用

     ```python
     def function_2(*args, **kwargs):
         print(args)
         print(kwargs)
     
     foo_2(1, 2, 3, a = 4, b = 5, c = 6)
     '''
     1 2 3
     {'a': 4, 'b': 5, 'c': 6}
     '''
     ```

#### 5.1.4 函数体与变量作用域

- 函数体就是一段只在函数被调用时，才会执行的代码，代码构成与其他代码并无不同

- `局部变量`——仅在函数体内定义和发挥作用

  ```python
  def multipy(x, y):
      z = x * y
      return z
  
  print(multipy(3, 9))
  ```

- `全局变量`——外部定义的都是全局变量

  - 全局变量可以在函数体内直接被使用

    ```python
    n = 3
    ls = [0]
    def multipy_2(x, y):
        z = n * x * y
        ls.append(z)
        return z
    print(multipy_2(2, 9))
    print(ls)
    '''
    54
    [0, 54]
    '''
    ```

  - 通过global在函数体内定义全局变量

    ```python
    ls = [0]
    def multipy_2(x, y):
        global z
        z = x * y
        return z
    print(multipy_2(2, 9)) # 18
    print(z) # 18
    ```

#### 5.1.5 返回值

1. 单个返回值

2. 多个返回值——以元组的形式

   ```python
   def foo_4(x = 1):
       return 1, x, x**2, x**3
   print(foo_4(3))
   a, b, c, d = foo_4(3)
   print(a)
   print(b)
   print(c)
   print(d)
   '''
   (1, 3, 9, 27)
   1
   3
   9
   27
   '''
   ```

3. 可以有多个return语句，一旦其中一个执行，代表了函数运行的结束

4. 没有return语句，返回值为None

#### 5.1.6 一些建议

1. 函数及其函数的明明参照变量的命名
2. 应包含简要阐述函数功能的注释，注释紧跟函数定义后面
3. 函数定义前后各空两行
4. 默认参数赋值等号两侧不需加空格



---

### 5.2 函数式编程实例

![image-20230313152156708](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303131521844.png)

- 单元测试——assert断言

  ```python
  def game_over(score_A, score_B):
      '''
      单场模拟结束条件，一方先达到21分，比赛结束
      :param score_A:
      :param score_B:
      :return: True or False: 是否结束单场比赛
      '''
      return score_A == 21 or score_B == 21
  
  
  # 单元测试——assert
  assert game_over(21, 8)
  assert game_over(9, 21)
  assert game_over(9 ,9) # 表达式结果为false时，触发异常AssertionError
  '''
  Traceback (most recent call last):
    File "E:/workplace_ZLY/codeMore/python/pythonProject_studyDeepLearning/01-studyPython/2022-03-20_pre/2023-03-13_02.py", line 86, in <module>
      assert game_over(9 ,9)
  AssertionError
  '''
  ```

- 实例

  ```python
  def main():
      '''
      主要逻辑
      :return: 
      '''
      # 获取原始数据
      probability_A, probability_B, number_of_game = get_inputs()
      # 获取模拟的结果
      win_A, win_B = result_n_game(probability_A, probability_B, number_of_game)
      # 结果汇总输出
      print_summary(win_A, win_B, number_of_game) 
  
  
  def get_inputs():
      '''
      输入原始数据：
      probability_A：A每球获胜的概率
      probability_B：B每球获胜的概率
      number_of_game：模拟的场次
      :return:
      '''
      probability_A = eval(input("请输入运动员A每球获胜的概率（0-1）："))
      probability_B = eval(input("请输入运动员B每球获胜的概率（0-1）："))
      number_of_game = eval(input("请输入模拟的场次（正整数）："))
  
      print("模拟比赛总次数：", number_of_game)
      print("A选手每球的获胜概率：", probability_A)
      print("B选手每球的获胜概率：", probability_B)
      return probability_A, probability_B, number_of_game
  
  
  def result_n_game(probability_A, probability_B, number_of_game):
      '''
      模拟多场比赛的结果
      :param probability_A:
      :param probability_B:
      :param number_of_game:
      :return: win_A: A获胜场次; win_B: B获胜场次
      '''
      win_A, win_B = 0, 0
      for i in range(number_of_game):
          score_A, score_B = result_one_game(probability_A, probability_B) # 模拟一次比赛的比分
          if score_A > score_B:
              win_A += 1
          else:
              win_B += 1
      return win_A, win_B
  
  
  import random
  def result_one_game(probability_A, probability_B):
      '''
      模拟一场比赛的结果
      :param probability_A:
      :param probability_B:
      :return: score_A: A的得分; score_B: B的得分
      '''
      score_A, score_B = 0, 0
      while not game_over(score_A, score_B):
          # random.random()产生[0, 1)之间的随机小数，均匀分布
          if random.random() < probability_A:
              score_A += 1
          else:
              score_B += 1
      return score_A, score_B
  
  
  def game_over(score_A, score_B):
      '''
      单场模拟结束条件，一方先达到21分，比赛结束
      :param score_A:
      :param score_B:
      :return: True or False: 是否结束单场比赛
      '''
      return score_A == 21 or score_B == 21
  
  
  def print_summary(win_A, win_B, number_of_game):
      '''
      结果汇总输出
      :param win_A:
      :param win_B:
      :param number_of_game:
      :return:
      '''
      print("共模拟了{}场比赛".format(number_of_game))
      print("选手A获胜{0}场，占比{1:.1%}".format(win_A, win_A/number_of_game))
      print("选手B获胜{0}场，占比{1:.1%}".format(win_B, win_B/number_of_game))
  
  
  main()
  ```



---

### 5.3 匿名函数

![image-20230313152224327](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303131522384.png)

1. 基本形式

   lambda 变量: 函数体

2. 常用语法

   在参数列表中最适合使用匿名函数，尤其是与 key = 搭配

   - 排序sort()，sorted()

     ```python
     ls = [(93, 88), (79, 100), (86, 71), (85, 95), (76, 94)]
     # 默认根据第一个元素进行排序
     ls.sort()
     print(ls) # [(76, 94), (79, 100), (85, 95), (86, 71), (93, 88)]
     ```

     ```python
     ls = [(93, 88), (79, 100), (86, 71), (85, 95), (76, 94)]
     # 按照key设置的量进行排序
     # x表示可迭代对象里的每个元素
     # x[1]表示第一个位置的元素进行排序
     ls.sort(key = lambda x:x[1])
     print(ls) # [(86, 71), (93, 88), (76, 94), (85, 95), (79, 100)]
     ```

     ```python
     ls = [(93, 88), (79, 100), (86, 71), (85, 95), (76, 94)]
     # sorted是一次临时排序
     temp = sorted(ls, key=lambda x: x[1])
     print(temp) # [(86, 71), (93, 88), (76, 94), (85, 95), (79, 100)]
     print(ls) # [(93, 88), (79, 100), (86, 71), (85, 95), (76, 94)]
     ```

     ```python
     ls = [(93, 88), (79, 100), (86, 71), (85, 95), (76, 94)]
     # 按照总成绩进行排序（降序）
     temp = sorted(ls, key=lambda x: x[0] + x[1], reverse=True)
     print(temp) # [(93, 88), (85, 95), (79, 100), (76, 94), (86, 71)]
     ```

   - max()，min()

     ```python
     ls = [(93, 88), (79, 100), (86, 71), (85, 95), (76, 94)]
     # 第二个元素最大
     max_num = max(ls, key=lambda x:x[1])
     # 第二个元素最小
     min_num = min(ls, key=lambda x:x[1])
     print(max_num) # (79, 100)
     print(min_num) # (86, 71)
     ```



---

### 5.4 面向过程和面向对象

`面向过程`：以过程为中心的编程思想，以“什么正在发生”为主要目标进行编程。（**冰冷的，程序化的**）

`面向对象`：以现实世界的事物抽象为对象，更关注“谁在受影响”，更贴近现实。（**有血有肉的，拟人化的**）



## 6. 类——面向对象的编程

![image-20230313152428940](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303131524013.png)

面向对象更符合人类对客观世界的抽象和理解

类是对象的载体

```python
# 用类创建实例
my_cat = Cat("Loser")
your_cat = Cat("Lucky")

# 调用属性
print(my_cat.name)
print(your_cat.name)

# 调用方法
my_cat.jump()
your_cat.jump()
'''
Loser
Lucky
Loseris jumping
Luckyis jumping
'''
```

---

### 6.1 类的定义

![image-20230313212159719](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303132121925.png)

三要素：类名、属性、方法

#### 6.1.1 类的命名

- 要有实际意义
- 驼峰命名法——组成的单词首字母大写

#### 6.1.2 类的属性

```python
def __init__(self, 要传递的参数): # 初始化类的属性
```

```python
class Car():
    def __init__(self, brand, model, year):
        '''初始化汽车属性'''
        self.brand = brand
        self.model = model
        self.year = year
        self.mileage = 0 # 新车总里程初始化为0
```

#### 6.1.3 类的方法

```
相当于内部定义的函数
```

```python
class Car():
    def __init__(self, brand, model, year):
        '''初始化汽车属性'''
        self.brand = brand
        self.model = model
        self.year = year
        self.mileage = 0 # 新车总里程初始化为0
    
    def get_main_information(self): # self不能省
        '''获取汽车的主要信息'''
        print("品牌：{}, 型号：{}, 出场年份：{}".format(self.brand, self.model, self.year))
    
    def get_mileage(self):
        '''获取总里程数'''
        return "行车总里程：{}公里".format(self.mileage)
```



---

### 6.2 创建实例

![image-20230313212222024](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303132122109.png)

#### 6.2.1 实例的创建

将实例赋值给对象，实例化过程中，传入相应的参数

v = 类名（必要的初始化参数）

```python
my_new_car= Car("Audi", "A6", 2018)
```

#### 6.2.2 访问属性

类名.属性名

```python
print(my_new_car.brand)
print(my_new_car.model)
print(my_new_car.year)
```

#### 6.2.3 调用方法

```python
# 调用方法
my_new_car.get_main_information()
mileage = my_new_car.get_mileage()
print(mileage)
```

#### 6.2.4 修改属性

1. 直接修改

   ```python
   my_old_car = Car("BYD", "宋", 2016)
   my_old_car.mileage = 120000
   print(my_old_car.get_mileage())
   ```

2. 通过方法修改属性

   ```python
   class Car():
       def __init__(self, brand, model, year):
           '''初始化汽车属性'''
           self.brand = brand
           self.model = model
           self.year = year
           self.mileage = 0 # 新车总里程初始化为0
   
       def get_main_information(self): # self不能省
           '''获取汽车的主要信息'''
           print("品牌：{}, 型号：{}, 出场年份：{}".format(self.brand, self.model, self.year))
   
       def get_mileage(self):
           '''获取总里程数'''
           return "行车总里程：{}公里".format(self.mileage)
   
       def set_mileage(self, mileage):
           '''设置总里程数'''
           self.mileage = mileage
   
   my_new_car.set_mileage(200000)
   print(my_new_car.get_mileage())
   ```

3. 继续拓展

   - 禁止设置负里程

     ```python
     class Car():
         def __init__(self, brand, model, year):
             '''初始化汽车属性'''
             self.brand = brand
             self.model = model
             self.year = year
             self.mileage = 0 # 新车总里程初始化为0
     
         def get_main_information(self): # self不能省
             '''获取汽车的主要信息'''
             print("品牌：{}, 型号：{}, 出场年份：{}".format(self.brand, self.model, self.year))
     
         def get_mileage(self):
             '''获取总里程数'''
             return "行车总里程：{}公里".format(self.mileage)
     
         def set_mileage(self, distance):
             '''设置总里程数'''
             if distance > 0:
                 self.mileage = distance
             else:
                 print("里程数不能为负")
     ```

   - 将每次的里程数累加

     ```python
     class Car():
         def __init__(self, brand, model, year):
             '''初始化汽车属性'''
             self.brand = brand
             self.model = model
             self.year = year
             self.mileage = 0 # 新车总里程初始化为0
     
         def get_main_information(self): # self不能省
             '''获取汽车的主要信息'''
             print("品牌：{}, 型号：{}, 出场年份：{}".format(self.brand, self.model, self.year))
     
         def get_mileage(self):
             '''获取总里程数'''
             return "行车总里程：{}公里".format(self.mileage)
     
         def set_mileage(self, distance):
             '''设置总里程数'''
             if distance > 0:
                 self.mileage = distance
             else:
                 print("里程数不能为负")
     
         def increase_mileage(self, distance):
             '''总里程数累计'''
             if distance > 0:
                 self.mileage += distance
             else:
                 print("新增里程数不能为负")
     ```

> `小结`：
>
> - 包含的信息可以是极大的，可以创建无穷多的实例
> - 高度的拟人（物）化，符合人类对客观世界的抽象和理解



---

### 6.3 类的继承

![image-20230313212249536](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303132122633.png)

#### 6.3.1 简单的继承

- 父类

  ```python
  class Car():
      def __init__(self, brand, model, year):
          '''初始化汽车属性'''
          self.brand = brand
          self.model = model
          self.year = year
          self.mileage = 0 # 新车总里程初始化为0
  
      def get_main_information(self): # self不能省
          '''获取汽车的主要信息'''
          print("品牌：{}, 型号：{}, 出场年份：{}".format(self.brand, self.model, self.year))
  
      def get_mileage(self):
          '''获取总里程数'''
          return "行车总里程：{}公里".format(self.mileage)
  
      def set_mileage(self, distance):
          '''设置总里程数'''
          if distance > 0:
              self.mileage = distance
          else:
              print("里程数不能为负")
  
      def increase_mileage(self, distance):
          '''总里程数累计'''
          if distance > 0:
              self.mileage += distance
          else:
              print("新增里程数不能为负")
  ```

- 子类

  class 子类名(父类名): 

  ```python
  class ElectricCar(Car):
      '''模拟电动汽车'''
      def __init__(self, brand, model, year):
          '''初始化汽车属性'''
          super().__init__(brand, model, year) # 声明继承父类的属性
  
  my_electric_car = ElectricCar("FF91", "Tomorrow", 2048)
  my_electric_car.get_main_information() # 品牌：FF91, 型号：Tomorrow, 出场年份：2048
  ```

#### 6.3.2 给子类添加属性和方法

```python
class ElectricCar(Car):
    '''模拟电动汽车'''

    def __init__(self, brand, model, year, battery_size):
        '''初始化汽车属性'''
        super().__init__(brand, model, year)  # 声明继承父类的属性
        self.battery_size = battery_size  # 电池容量
        self.electric_quantity = battery_size  # 电池剩余电量
        self.electric2distance_ratio = 5  # 点亮距离换算系数 5公里/kw·h
        self.remainder_range = self.electric_quantity * self.electric2distance_ratio  # 剩余可行驶里程

    def get_electric_quantity(self):
        '''查看当前电池剩余电量'''
        print("当前电池剩余电量：{}kw·h".format(self.electric_quantity))

    def set_electric_quantity(self, electric_quantity):
        '''设置电池剩余电量，重新计算电量可制成行驶历程'''
        if electric_quantity >= 0 and electric_quantity <= self.battery_size:
            self.electric_quantity = electric_quantity
            self.remainder_range = self.electric_quantity * self.electric2distance_ratio
        else:
            print("电量未设置合理范围")

    def get_remainder_range(self):
        '''查看剩余可行使历程'''
        print("当前电量还可以继续行驶{}公里".format(self.remainder_range))


my_electric_car = ElectricCar("FF91", "Tomorrow", 2048, 70)
my_electric_car.get_electric_quantity()  # 获取当前电池电量
my_electric_car.get_remainder_range()  # 获取当前剩余可行使里程

# 重设电池电量
my_electric_car.set_electric_quantity(50)
my_electric_car.get_electric_quantity()
my_electric_car.get_remainder_range()
```

#### 6.3.3 重写父类的方法——多态

```python
class ElectricCar(Car):
    '''模拟电动汽车'''

    def __init__(self, brand, model, year, battery_size):
        '''初始化汽车属性'''
        super().__init__(brand, model, year)  # 声明继承父类的属性
        self.battery_size = battery_size  # 电池容量
        self.electric_quantity = battery_size  # 电池剩余电量
        self.electric2distance_ratio = 5  # 点亮距离换算系数 5公里/kw·h
        self.remainder_range = self.electric_quantity * self.electric2distance_ratio  # 剩余可行驶里程

    def get_main_information(self):
        '''获取汽车主要信息'''
        print("品牌：{}，型号：{}，出厂年份：{}，续航里程：{}公里".format(self.brand, self.model, self.year,
                                                     self.electric_quantity * self.electric2distance_ratio))

    def get_electric_quantity(self):
        '''查看当前电池剩余电量'''
        print("当前电池剩余电量：{}kw·h".format(self.electric_quantity))

    def set_electric_quantity(self, electric_quantity):
        '''设置电池剩余电量，重新计算电量可制成行驶历程'''
        if electric_quantity >= 0 and electric_quantity <= self.battery_size:
            self.electric_quantity = electric_quantity
            self.remainder_range = self.electric_quantity * self.electric2distance_ratio
        else:
            print("电量未设置合理范围")

    def get_remainder_range(self):
        '''查看剩余可行使历程'''
        print("当前电量还可以继续行驶{}公里".format(self.remainder_range))
```

#### 6.3.4 用在类当中脑袋实例

> 把电池抽象成一个对象
>
> 逻辑更加清晰

```python
class Battery():
    '''模拟电动车的电池'''

    def __init__(self, battery_size=70):
        self.battery_size = battery_size  # 电池容量
        self.electric_quantity = battery_size  # 电池剩余电量
        self.electric2distance_ratio = 5  # 电池距离换算系数 5公里/kw·h
        self.remainder_range = self.electric_quantity * self.electric2distance_ratio  # 剩余可行使里程

    def get_electric_quantity(self):
        '''查看当前电池电量'''
        print("当前电池剩余电量：{}".format(self.electric_quantity))

    def set_electric_quantity(self, electric_quantity):
        '''设置电池剩余电量，重新计算电量可支撑里程'''
        if electric_quantity >= 0 and electric_quantity <= self.battery_size:
            self.electric_quantity = electric_quantity
            self.remainder_range = self.electric_quantity * self.electric2distance_ratio
        else:
            print("电量未设置在合理范围")

    def get_remainder_range(self):
        '''查看剩余可行使历程'''
        print("当前电量还可以继续行驶{}公里".format(self.remainder_range))


class ElectricCar(Car):
    '''模拟电动汽车'''

    def __init__(self, brand, model, year, battery_size):
        '''初始化汽车属性'''
        super().__init__(brand, model, year)  # 声明继承父类的属性
        self.battery = Battery(battery_size)

    def get_main_information(self):
        '''获取汽车主要信息'''
        print("品牌：{}，型号：{}，出厂年份：{}，续航里程：{}公里".format(self.brand, self.model, self.year,
                                                     self.battery.electric_quantity * self.battery.electric2distance_ratio))

    def get_electric_quantity(self):
        '''查看当前电池剩余电量'''
        print("当前电池剩余电量：{}kw·h".format(self.battery.electric_quantity))

    def set_electric_quantity(self, electric_quantity):
        '''设置电池剩余电量，重新计算电量可制成行驶历程'''
        self.battery.set_electric_quantity(electric_quantity)

    def get_remainder_range(self):
        '''查看剩余可行使历程'''
        self.battery.get_remainder_range()
```



## 7. 文件、异常和模块

![image-20230313212424233](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303132124325.png)

实际应用中，我们绝大多数的数据都是通过文件的交互完成的

### 7.1 文件的读写

![image-20230315140051385](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303151400603.png)

#### 7.1.1 文件的打开

- 文件的打开通用格式

  ```python
  with open("文件路径", "打开模式", encoding="操作文件的字符编码") as f: "对文件进行相应的读写操作"
  ```

  使用with块的好处：执行完毕后，自动对文件进行close操作

  - 【例】简单的文件读取

    ```python
    with open("E:\workplace_ZLY\testDocument\testTxt_01.txt", "r", encoding="UTF-8") as f: 
        text = f.read() 
    '''输入格式错误 Invalid argument'''
    
    '''使用 \\ 或 /'''
    with open("E:\\workplace_ZLY\\testDocument\\testTxt_01.txt", "r", encoding="UTF-8") as f: 
        text_01 = f.read()
    with open("E:/workplace_ZLY/testDocument/testTxt_01.txt", "r", encoding="UTF-8") as f: 
        text_02 = f.read()
    print(text_01)
    print(text_02)
    ```

1. 文件路径

   - 完整的文件路径

     如上例 E:\\workplace_ZLY\\testDocument\\testTxt_01.txt

   - 程序与文件在同一文件夹，可简化成文件名

     ![image-20230315093753377](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303150938169.png)

     ```python
     '''
     @Project ：pythonProject_studyDeepLearning 
     @File    ：2023-03-15_01.py
     @IDE     ：PyCharm 
     @Author  ：DueFireTop
     @Date    ：2023/3/15 9:20 
     '''
     with open("textFile.txt", "r", encoding="UTF-8") as f: 
         text = f.read()
     print(text)
     ```

2. 打开模式

   - `r`：只读模式，如果文件不存在，报错
   - `w`：覆盖写模式，如果文件不存在，则创建；如果文件存在，则完全覆盖原文件
   - `x`：创建写模式，如果文件不存在，则创建；如果文件存在，则报错
   - `a`：追加写模式，如果文件不存在，则创建；如果文件存在，则在原文件后追加内容
   - `b`：二进制文件模式，不能单独使用，需要配合使用如`rb`、`wb`、`ab`，该模式不需要指定encoding
   - `t`：文本文件模式，默认值，需配合使用如`rt`，`wt`，`at`，一般省略，简写成如`r`，`w`，`a`
   - `+`：与`r`，`w`，`x`，`a`配合使用，在原功能的基础上，增加读写功能
   - 打开模式缺省，默认为只读模式

3. 字符编码

   - 万国码：utf-8

     包含世界上所有国家语言的字符

   - 中文编码：gbk

     专门解决中文编码问题

   - 在windows系统下，如果缺省，则默认为gbk（所在区域编码）

   - 为清楚起见，除了处理二进制文件，建议不要缺省encoding

#### 7.1.2 文件的读取

1. 读取整个内容——f.read()

   ```python
   with open("E:\\workplace_ZLY\\testDocument\\testTxt_01.txt", "r", encoding="UTF-8") as f: 
       text_01 = f.read()
   with open("E:/workplace_ZLY/testDocument/testTxt_01.txt", "r", encoding="UTF-8") as f: 
       text_02 = f.read()
   print(text_01)
   print(text_02)
   ```

   - 解码模式不匹配

     ```python
     with open("E:/workplace_ZLY/testDocument/testTxt_01.txt", "r", encoding="gbk") as f: 
         text_03 = f.read()
     print(text_03)
     '''
     UnicodeDecodeError: 'gbk' codec can't decode byte 0x84 in position 20: incomplete multibyte sequence
     '''
     ```

2. 逐行进行读取——f.readline()

   ```python
   # 该文件和python文件在同一个文件夹内
   with open("textFile.txt", "r", encoding="UTF-8") as f:
       text_04_01 = f.readline()
       text_04_02 = f.readline()
       text_04_03 = f.readline()
       text_04_04 = f.readline()
       
   # 保持原文的换行，使print()的换行不起作用
   print(text_04_01, end="")
   print(text_04_02)
   print(text_04_03, end="")
   print(text_04_04)
   
   print("-----------------------")
   
   with open("textFile.txt", "r", encoding="UTF-8") as f:
       while True:
           text = f.readline()
           if not text:
               break
           else:
               print(text, end="") 
   '''
   这是测试文件第一行
   第二行
   
   第三行
   第四行
   -----------------------
   这是测试文件第一行
   第二行
   第三行
   第四行
   '''
   ```

3. 读入所有行，以每行为元素，形成一个列表——f.readlines()

   ```python
   with open("textFile.txt", "r", encoding="UTF-8") as f:
       text_05 = f.readlines()
   print(text_05)
   
   print("-----------------------")
   
   with open("textFile.txt", "r", encoding="UTF-8") as f:
       for text_06 in f.readlines():
           print(text_06, end="")
   '''
   ['这是测试文件第一行\n', '第二行\n', '第三行\n', '第四行']
   -----------------------
   这是测试文件第一行
   第二行
   第三行
   第四行
   '''
   ```

4. 文本文件读取小结

   文件比较大时，read()和readlines()占用内存过大，不建议使用

   readline()用起来又不太方便

   ```python
   with open("textFile.txt", "r", encoding="UTF-8") as f:
       # f 本身就是一个可迭代对象，每次迭代读取一行内容
       for text_07 in f:
           print(text_07)
   '''
   这是测试文件第一行
   
   第二行
   
   第三行
   
   第四行
   '''
   ```

5. 二进制文件

   ```python
   with open("C:\\Users\\Administrator\\AppData\\Roaming\\Typora\\typora-user-images\\image-20230314205922652.png", "rb") as f:
       print(len(f.readlines())) # 321
   ```

#### 7.1.3 文件的写入

1. 向文件写入一个字符串或字节流（二进制）——f.write()

   ```python
   with open("textFile.txt", "w", encoding="UTF-8") as f:
       '''
           w
           文件不存在则创建一个
           如需换行，末尾加换行符 \n
           如果文件存在，新写入的内容会被覆盖掉，一定要【注意】
       '''
       f.write("这是我写入的第一行\n")
       f.write("这是我写入的第二行\n")
       f.write("这是我写入的第三行\n")
       f.write("这是我写入的第四行\n")
   ```

2. 追加模式——"a"

   ```python
   with open("textFile.txt", "a", encoding="UTF-8") as f:
       '''
           a
           文件不存在则创建一个
           如果文件存在，新写入内容会追加在原内容之后
       '''
       f.write("这是我新写入的第一行\n")
       f.write("这是我新写入的第二行\n")
       f.write("这是我新写入的第三行\n")
       f.write("这是我新写入的第四行\n")
   ```

3. 将一个元素为字符串的列表整体写入文件——f.writelines()

   ```python
   ls = ["字符串列表1", "字符串列表2", "字符串列表3", "字符串列表4"]
   with open("textFile.txt", "w", encoding="UTF-8") as f:
       f.writelines(ls)
   ```

   ![image-20230315101934948](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303151019987.png)

   ```python
   ls = ["字符串列表1\n", "字符串列表2\n", "字符串列表3\n", "字符串列表4\n"]
   with open("textFile.txt", "w", encoding="UTF-8") as f:
       f.writelines(ls)
   ```

   ![image-20230315102022688](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303151020727.png)

#### 7.1.4 既读又写

1. `r+`

   - 如果文件名不存在，则报错
   - 指针在开始
   - 要把指针移到末尾才能开始写，否则会覆盖前面内容

   ```python
   with open("textFile.txt", "r+", encoding="UTF-8") as f:
       # 将指针移到末尾 f.seek(偏移字节数, 位置（0：开始；1：当前位置；2：结尾）)
       f.seek(0, 2)
       text = ["r+新加内容f.seek_1\n", "r+新加内容f.seek_2\n"]
       f.writelines(text)
   
   print("--------这是全部读一遍，然后指针到达末尾----------")
   with open("textFile.txt", "r+", encoding="UTF-8") as f:
       # 全部读一边后，指针到达末尾
       for line in f:
           # print(line)
           continue
       text = ["r+新加内容1\n", "r+新加内容2\n"]
       f.writelines(text)
   ```

   ![image-20230315102927016](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303151029070.png)

2. `w+`

   - 若文件不存在，则创建
   - 若文件存在，会立刻【清空】原内容

   ```python
   with open("textFile.txt", "w+", encoding="UTF-8") as f:
       text = ["w+新加内容1\n", "w+新加内容2\n"]
       f.writelines(text)
       f.seek(0, 0) # 指针移到开始位置
       print(f.read()) # 读取内容
   ```

   ![image-20230315103248432](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303151032485.png)

3. `a+`

   - 若文件不存在，则创建
   - 指针自动在末尾，添加新内容，不会清空原内容

   ```python
   with open("textFile.txt", "a+", encoding="UTF-8") as f:
       text = ["a+新加内容1\n", "a+新加内容2\n"]
       f.writelines(text)
       f.seek(0, 0)
       print(f.read()) # 读取内容
   ```

   ![image-20230315103509032](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303151035076.png)

#### 7.1.5 数据的存储和读取

通用的数据格式，可以在不同语言中加载和存储

本节简单了解两种数据存储结构 csv 和 json

1. csv格式

   由逗号将数据分开的字符序列，可以由excel打开

   - 读取

     ![image-20230315105259584](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303151052623.png)

     ```python
     with open("Grade.csv", "r", encoding="UTF-8") as f:
         ls = []
         # 逐行读取
         for line in f:
             # 去掉每行的换行符，然后用 “,” 进行分割
             ls.append(line.strip("\n").split(",")) 
         for res in ls:
             print(res)
     '''
     ['编号', '数学成绩', '语文成绩']
     ['1', '100', '98']
     ['2', '96', '99']
     ['3', '97', '95']
     '''
     ```

   - 写入

     ```python
     ls = [['编号', '数学成绩', '语文成绩'], ['4', '55', '89'], ['5', '99', '32']]
     with open("Grade.csv", "w", encoding="UTF-8") as f:
         # 逐行写入
         for row in ls:
             # 用逗号组合字符串形式，末尾加换行符
             f.write(",".join(row) + "\n")
     ```

     ![image-20230315105640441](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303151056480.png)

   也可以借助csv模块完成上述操作

2. json格式

   常被用来存储字典类型

   - 写入——dump()

     ```python
     import json
     scores = {
         "Peter":{"Math": 96, "Physics": 98},
         "Paul":{"Math": 97, "Physics": 89},
         "Marry":{"Math": 56, "Physics": 88},
               }
     
     # 写入整个对象
     with open("score.json", "w", encoding="utf-8") as f:
         # indent表示字符串换行＋缩进，ensure_ascii 显示中文
         json.dump(scores, f, indent=4, ensure_ascii=False)
     ```

     ![image-20230315110325624](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303151103672.png)

   - 读取——load()

     ```python
     # 加载整个对象
     with open("score.json", "r", encoding="utf-8") as f:
         scores = json.load(f)
         for k, v in scores.items():
             print(k, v)
     '''
     Peter {'Math': 96, 'Physics': 98}
     Paul {'Math': 97, 'Physics': 89}
     Marry {'Math': 56, 'Physics': 88}
     '''
     ```



---

### 7.2 异常处理

![image-20230315140220883](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303151402967.png)

#### 7.2.1 常见异常的产生

1. 除0运算——ZeroDivisionError: division by zero

2. 找不到可读文件——FileNotFoundError: [Errno 2] No such file or directory

3. 值错误——ValueError: invalid literal for int() with base 10

   传入一个调用者不期望的值，即使这个值的类型是正确的

   ```python
   s = "1.3"
   n = int(s)
   ```

4. 索引错误——IndexError: list index out of range

   下标超出序列边界

   ```python
   ls = [1, 2, 3]
   print(ls[5])
   ```

5. 类型错误——TypeError: unsupported operand type(s) for +

   传入对象类型与要求不符

   ```python
   print(1 + "3")
   ```

6. 其他常见的异常类型

   NameError 使用一个还未被赋予对象的变量

   KeyError 试图访问字典例不存在的键

当异常发生的时候，如果不预先设定处理方法，程序就会中断

#### 7.2.2 异常的处理

> 提高程序的稳定性和可靠性

1. try_except

   ```
   如果 try 内的代码块顺利执行，except不被触发
   如果 try 内的代码块发生错误，出发except，执行except内代码块
   ```

   - 单分支

     ```python
     x = 10
     y = 0
     
     try:
         z = x / y
     except ZeroDivisionError:
         '''
             一般来说会预判出现什么异常
             如果预判错了，还是会抛出异常
         '''
         print("0不可以被整除")
     ```

   - 多分支

     ```python
     ls = []
     d = {"Name": "大眼仔"}
     try:
         print(d["age"])
     except NameError:
         print("变量名不存在")
     except IndexError:
         print("索引超出界限")
     except KeyError:
         print("键不存在")
     ```

   - 万能异常 Exception（所有错误的父类）

     ```python
     ls = []
     d = {"Name": "大眼仔"}
     try:
         print(d["age"])
     except Exception:
         print("出现异常")
     ```

   - 捕获异常的值

     ```python
     try:
         y = m
     except Exception as e:
         # 虽然不能获得错误的具体类型，但是可以获得错误的值
         print(e)
     '''
     name 'm' is not defined
     '''
     ```

2. try_except_else

   - 如果try模块执行，则else模块也执行

   - 可以将else看作try成功的额外奖赏

     ```python
     try:
         with open("textFile.txt", "r", encoding="utf-8") as f:
             test = f.read()
     except FileNotFoundError:
         print("找不到该文件")
     else:
         for s in ["\n", ", ", "。", "?"]:
             # 去掉换行符和标点符号
             test = test.replace(s, "")
         print("这个文件由{}个字符组成".format(len(test)))
     ```

3. try_except_finally

   - 不论try模块是否执行，finally最后都执行

     ```python
     ls = []
     d = {"Name": "大眼仔"}
     try:
         y = x
         ls[3]
         d["age"]
     except Exception as e:
         print(e)
     finally:
         print("布林是否触发异常，都会执行")
     ```



---

### 7.3 模块简介

已经封装好

无需自己再造轮子

声明导入后，拿来即用

![image-20230315140304653](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303151403737.png)

#### 7.3.1 广义模块分类

1. Python内置

   时间库time；随即库random；容器数据类型collection；迭代器函数itertools

2. 第三方库

   数据分析numpy、pandas；数据可视化matplotlib；机器学习scikit-learn；深度学习Tensorflow

3. 自定义文件

   - 单独py文件
   - 包——多个py文件

#### 7.3.2 模块的导入

1. 导入整个模块——import 模块名

   调用方式：模块名.函数名或类名

   ```python
   import time
   start = time.time()
   time.sleep(3)
   end = time.time()
   print("程序运行时间：{:.2f}秒".format(end - start))
   ```

2. 从模块中导入类或函数——from 模块 import 类名或函数名

   调用方式：函数名或类名

   ```python
   from itertools import product
   # 笛卡尔积
   ls = list(product("AB", "123"))
   print(ls)
   '''
   [('A', '1'), ('A', '2'), ('A', '3'), ('B', '1'), ('B', '2'), ('B', '3')]
   '''
   ```

   一次导入多个

   ```python
   from function import fun1, fun2
   fun1.f1()
   fun2.f2()
   ```

3. 导入模块中所有的类和函数——from 模块 import

   调用方式：函数名或类名

   ```python
   from random import *
   print(randint(1, 100))
   print(random())
   ```

#### 7.3.3 模块的查找路径

模块搜索查找顺序：

1. 内存中已经加载的模块

2. 内置模块

3. sys.path路径中包含的模块

   ```python
   import sys
   
   print(sys.path)
   ```

   - sys.path的第一个路径是当前执行文件所在的文件夹
   - 若需要将不在该文件内的模块导入，需要将模块的路径添加到sys.path



## 8. 有益的探索

![ ](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303151406769.png)

### 8.1 数据类型的底层实现

#### 8.1.1 从奇怪的列表说起

1. 错综复杂的复制

   ```python
   list_1 = [1, {22, 3, 44}, (5, 6, 7), {"name": "Sarah"}]
   ```

   - 浅拷贝

     ```python
     list_2 = list_1.copy()
     print(list_2)
     
     list_3 = list_1[:]
     print(list_3)
     
     list_4 = list(list_1)
     print(list_4)
     ```

   - 对浅拷贝前后两列表分别进行操作

     ```python
     list_2[1].append(55)
     print("list_2 = ", list_2)
     print("list_1 = ", list_1)
     '''
     list_2 =  [1, [22, 3, 44, 55], (5, 6, 7), {'name': 'Sarah'}]
     list_1 =  [1, [22, 3, 44, 55], (5, 6, 7), {'name': 'Sarah'}]
     '''
     ```

2. 列表的底层实现

   <img src="https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221520385.png" alt="image-20230322152037321" style="zoom:50%;" />

   列表内的元素可以分散的存储在内存中

   列表是采用引用数组（地址）

   列表存储的，实际上是这些元素的地址——地址的存储在内存中是连续的

   - 新增元素

     <img src="https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221523790.png" alt="image-20230322152317736" style="zoom:50%;" />

     <img src="https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221523092.png" alt="image-20230322152342031" style="zoom:50%;" />

     

     ```python
     list_1 = [1,[22, 3, 44], (5, 6, 7), {"name": "Sarah"}]
     list_2 = list(list_1)
     
     list_1.append(100)
     list_2.append("n")
     print("list_1 = ", list_1)
     print("list_2 = ", list_2)
     '''
     list_1 =  [1, [22, 3, 44], (5, 6, 7), {'name': 'Sarah'}, 100]
     list_2 =  [1, [22, 3, 44], (5, 6, 7), {'name': 'Sarah'}, 'n']
     '''
     ```

   - 修改元素

     <img src="https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221525829.png" alt="image-20230322152502764" style="zoom:50%;" />

     ```python
     list_1[0] = 10
     list_2[0] = 20
     print("list_1 = ", list_1)
     print("list_2 = ", list_2)
     '''
     list_1 =  [10, [22, 3, 44], (5, 6, 7), {'name': 'Sarah'}, 100]
     list_2 =  [20, [22, 3, 44], (5, 6, 7), {'name': 'Sarah'}, 'n']
     '''
     ```

   - 对列表型元素进行操作

     <img src="https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221527395.png" alt="image-20230322152736331" style="zoom:50%;" />

     <img src="https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221527462.png" alt="image-20230322152756399" style="zoom:50%;" />

     ```python
     list_1[1].remove(44)
     list_2[1] += [55, 66]
     print("list_1 = ", list_1)
     print("list_2 = ", list_2)
     '''
     list_1 =  [10, [22, 3, 55, 66], (5, 6, 7), {'name': 'Sarah'}, 100]
     list_2 =  [20, [22, 3, 55, 66], (5, 6, 7), {'name': 'Sarah'}, 'n']
     '''
     ```

   - 对元组型元素进行操作

     <img src="https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221529474.png" alt="image-20230322152941400" style="zoom:50%;" />

     ```python
     list_1 = [1,[22, 3, 44], (5, 6, 7), {"name": "Sarah"}]
     list_2 = list(list_1)
     
     list_2[2] += (8, 9)
     
     print("list_1 = ", list_1)
     print("list_2 = ", list_2)
     '''
     list_1 =  [10, [22, 3, 55, 66], (5, 6, 7), {'name': 'Sarah'}, 100]
     list_2 =  [20, [22, 3, 55, 66], (5, 6, 7, 8, 9), {'name': 'Sarah'}, 'n']
     '''
     ```

     元组是不可变的

   - 对字典型元素进行操作

     <img src="https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221531232.png" alt="image-20230322153154160" style="zoom:50%;" />

     ```python
     list_1 = [1,[22, 3, 44], (5, 6, 7), {"name": "Sarah"}, 100]
     list_2 = list(list_1)
     
     list_1[-2]["age"] = 19
     print("list_1 = ", list_1)
     print("list_2 = ", list_2)
     '''
     list_1 =  [10, [22, 3, 55, 66], (5, 6, 7), {'name': 'Sarah', 'age': 19}, 100]
     list_2 =  [20, [22, 3, 55, 66], (5, 6, 7, 8, 9), {'name': 'Sarah', 'age': 19}, 'n']
     '''
     ```

   

3. 引入深拷贝

   > 针对不可变元素（数字、字符串、元组）的操作，都各自生效了
   >
   > 针对不可变元素（列表、集合）的操作，发生了一些混淆

   - 深拷贝将所有层级的相关元素全部复制，完全分开，泾渭分明，避免了上述问题

   ```python
   import copy
   list_1 = [1,[22, 3, 44], (5, 6, 7), {"name": "Sarah"}]
   list_2 = copy.deepcopy(list_1)
   
   list_1[-1]["age"] = 18
   list_2[1].append(55)
   print("list_1 = ", list_1)
   print("list_2 = ", list_2)
   '''
   list_1 =  [1, [22, 3, 44], (5, 6, 7), {'name': 'Sarah', 'age': 18}]
   list_2 =  [1, [22, 3, 44, 55], (5, 6, 7), {'name': 'Sarah'}]
   '''
   ```

#### 8.1.2 神秘的字典

1. 快速的查找

   ```python
   import time
   
   ls_1 = list(range(1000000))
   ls_2 = list(range(500)) + [-50]*500
   
   start_time = time.time()
   
   count = 0
   for n in ls_2:
       if n in ls_1:
           count += 1
   
   end_time = time.time()
   print("查找{}个元素，在ls_1列表中的有{}个，共用时{}秒".format(len(ls_2), count, round(end_time - start_time)))
   
   print("---------------------------------")
   
   d = {i:i for i in range(1000000)}
   ls_2 = list(range(500)) + [-10]*500
   
   start_time = time.time()
   
   count = 0
   for n in ls_2:
       try:
           d[n]
       except:
           pass
       else:
           count += 1
   
   end_time = time.time()
   print("查找{}个元素，在ls_1列表中的有{}个，共用时{}秒".format(len(ls_2), count, round(end_time - start_time)))
   
   '''
   查找1000个元素，在ls_1列表中的有500个，共用时4秒
   ---------------------------------
   查找1000个元素，在ls_1列表中的有500个，共用时0秒
   '''
   ```

2. 字典的底层实现

   通过稀疏数组来实现值的存储与访问

   - 字典的创建过程

     1. 创建一个散列表（稀疏数组 N >> n）

        ```python
        d = {}
        ```

     2. 通过hash()计算键的散列值

        ```python
        print(hash("python"))
        print(hash(1024))
        print(hash((1, 2)))
        '''
        5251831232766238030
        1024
        -3550055125485641917
        '''
        ```

        ```python
        d["age"] = 18 # 增加键值对的操作，首先会计算散列值hash("age")
        print(hash("age"))
        print(d)
        '''
        -7565899355172206369
        {'age': 18}
        '''
        ```

     3. 根据计算的散列值确定其在散列表中的位置

        极个别的时候，散列值会发生冲突，则内部有相应的解决冲突的办法

     4. 在该位置上存入值

   - 键值对的访问过程

     <img src="https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221554211.png" alt="image-20230322155407142" style="zoom:50%;" />

     ```python
     d["age"]
     ```

     1. 计算要访问的键的散列值
     2. 根据计算的散列值，经过一定的规则，确定其在散列表中的位置
     3. 读取该位置上存储的值
        - 如果存在，则返回该值
        - 如果不存在，则报错KeyError

3. 小结

   - 字典数据类型，通过空间换时间，实现了快速的数据查找
     - 也就注定了字典的空间利用率低下
   - 因为散列值对应位置的顺序与键在字典中显示的顺序可能不同，因此表现出来的字典是无序的
     - 如果N = n，会产生很多位置冲突

#### 8.1.3 紧凑的字符串

通过紧凑组实现字符串的存储

![](https://bucket-zly.oss-cn-beijing.aliyuncs.com/img/Typora/202303221602755.png)

- 数据在内存中是连续存放的，效率更高，节省空间

#### 8.1.4 是否可变

1. 不可变类型：数字、字符串、元组

   在生命周期中保持内容不变

   - 换句话说，改变了就不是它自己了
   - 不可变对象 += 操作，实际上是创建了一个新的对象

   ```python
   x = 1
   y = "python"
   print(id(x))
   print(id(y))
   
   x += 2
   y += "3.7"
   print(id(x))
   print(id(y))
   '''
   140721843394288
   2110891472048
   140721843394352
   2110891916144
   '''
   ```

   元组并不总是不可变的

   ```python
   t = (1, [2])
   t[1].append(3)
   print(t)
   '''
   (1, [2, 3])
   '''
   ```

2. 可变类型：列表、字典、集合

   - id保持不变，但是里面的内容可以变
   - 可变对象的 += 操作，实际是在原对象的基础上就地修改

#### 8.1.5 列表操作的例子

1. 删除列表内的特定元素

   - 方法一：存在运算删除法

     缺点：每次存在运算，都要从头对列表进行遍历查找，效率低

     ```python
     alist = ["d", "d", "d", "d", "1", "2", "2", "d", "4", "d", "d"]
     s = "d"
     while True:
         if s in alist:
             alist.remove(s)
         else:
             break
     print(alist)
     ```

   - 方法二：一次性遍历元素执行删除

     ```python
     alist = ["d", "d", "d", "d", "1", "2", "2", "d", "4", "d", "d"]
     for s in alist:
         if s == "d":
             alist.remove(s) # 删除列表中第一次出现的该元素
     print(alist)
     '''
     ['1', '2', '2', 'd', '4', 'd', 'd']
     '''
     ```

   - 解决办法：使用负向索引

     ```python
     alist = ["d", "d", "d", "d", "1", "2", "2", "d", "4", "d", "d"]
     for i in range(-len(alist), 0):
         if alist[i] == "d":
             alist.remove(alist[i])
     print(alist)
     ```

2. 多维列表的创建

   ```python
   ls = [[0]*10]*5
   print(ls)
   print("---------------------")
   
   ls[0][0] = 1
   print(ls)
   '''
   [[0, 0, 0, 0, 0, 0, 0, 0, 0, 0], 
   [0, 0, 0, 0, 0, 0, 0, 0, 0, 0], 
   [0, 0, 0, 0, 0, 0, 0, 0, 0, 0], 
   [0, 0, 0, 0, 0, 0, 0, 0, 0, 0], 
   [0, 0, 0, 0, 0, 0, 0, 0, 0, 0]]
   ---------------------
   [[1, 0, 0, 0, 0, 0, 0, 0, 0, 0], 
   [1, 0, 0, 0, 0, 0, 0, 0, 0, 0], 
   [1, 0, 0, 0, 0, 0, 0, 0, 0, 0], 
   [1, 0, 0, 0, 0, 0, 0, 0, 0, 0], 
   [1, 0, 0, 0, 0, 0, 0, 0, 0, 0]]
   '''
   ```

---



### 8.2 更加简介的语法

#### 8.2.1 解析语法

```python
ls = [[0]*10 for i in range(5)]
print(ls)

print("---------------------")

ls[0][0] = 1
print(ls)
'''
[[0, 0, 0, 0, 0, 0, 0, 0, 0, 0], 
[0, 0, 0, 0, 0, 0, 0, 0, 0, 0], 
[0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
[0, 0, 0, 0, 0, 0, 0, 0, 0, 0], [
0, 0, 0, 0, 0, 0, 0, 0, 0, 0]]
---------------------
[[1, 0, 0, 0, 0, 0, 0, 0, 0, 0], 
[0, 0, 0, 0, 0, 0, 0, 0, 0, 0], 
[0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
[0, 0, 0, 0, 0, 0, 0, 0, 0, 0], 
[0, 0, 0, 0, 0, 0, 0, 0, 0, 0]]
'''
```

1. 解析语法的基本结构——以列表解析为例（也成为列表推导）

   [expression for value in iterable if condition]

   - 三要素：表达式、可迭代对象、if条件（可选）

   > 执行过程
   >
   > 1. 从可迭代对象中拿出一个元素
   > 2. 通过if条件（如果有的话），对元素进行筛选
   >    - 若通过筛选，则把元素传递给表达式
   >    - 若未通过，则进入 1 步骤，进行下一次迭代
   > 3. 将传递给表达式的元素，代入表达式进行处理，产生一个结果
   > 4. 将 3 步产生的结果作为列表的一个元素进行存储
   > 5. 重复 1-4 步，直至迭代对象迭代结束，返回新创建的列表
   >
   > ```python
   > # 等价于如下代码
   > result = []
   > for value in iterale:
   >     if condition:
   >         result.append(expression)
   > ```

   【例】求20以内的奇数的平方

   ```python
   squares = []
   for i in range(1, 21):
       if i % 2 == 1:
           squares.append(i**2)
   print(squares)
   '''
   [1, 9, 25, 49, 81, 121, 169, 225, 289, 361]
   '''
   ```

   ```python
   squares = [i**2 for i in range(1, 21) if i%2 == 1]
   print(squares)
   '''
   [1, 9, 25, 49, 81, 121, 169, 225, 289, 361]
   '''
   ```

   - 支持多变量

     ```python
     x = [1, 2, 3]
     y = [1, 2, 3]
     
     results = [i * j for i, j in zip(x, y)]
     print(results)
     '''
     [1, 4, 9]
     '''
     ```

   - 支持循环嵌套

     ```python
     colors = ["black", "white"]
     sizes = ["S", "M", "L"]
     t_shirt = ["{} {}".format(color, size) for color in colors for size in sizes]
     print(t_shirt)
     '''
     ['black S', 'black M', 'black L', 'white S', 'white M', 'white L']
     '''
     ```

2. 其他解析语法的例子

   35:03

3. 









































# 二、数据科学入门























