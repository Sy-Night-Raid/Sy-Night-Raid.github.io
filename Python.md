# 第一章 变量和简单数据类型
                  
## 0x0 简单的打印格式
```python
print("Hello Python World!")
```
## 0x1 变量
* 使用一个变量去存储一些信息    
```python
message = "Hello Python World!"
print(message)
```
**如果修改一下message变量的信息呢**
```python
message = "Hello Python World!"
print(message)

message = "Hello Python Crash Course World!"
print(message)
```
```python
输出的结果为 
Hello Python World!
Hello Python Crash Course World!
```
说明程序中可以随时修改变量的值，而python只会保留最新的变量值          

## 0x2 第一种数据类型———字符串
### 定义：字符串就是一系列字符
* 在python中，用引号括起的都是字符串（在python中单引号和双引号都是可以的）

### 修改字符串的大小写
1. 将每个单词首字母显示为大写的title()函数：
```python
name = "shaunt white"
print(name.title())

输出的结果为Shaunt White

# 在这个程序中，小写的字符串shaunt white存储到了变量name中，在print中，方法title()出现在了
变量的后面（方法是Python可对数据执行的操作），每个方法后面都跟着一对括号，这样因为有的方法需要额外的信息来完成工作，
但title()明显不需要额外的信息
```
2. 将字符串全部显示为大写或小写的函数upper()和lower():
```python
name = "shaunt white"
print(name.upper())
print(name.lower())

输出结果为
SHAUNT WHITE
shaunt white
```

### 合并（拼接）字符串
* Python使用加号（+）来合并字符串
```python
first_name = "roy"
last_name = "miller"
full_name = first_name + "  " + last_name
print(full_name.title())

输出的结果为
Roy Miller
若没有中间的字符串空格的话，输出的结果为
Roymiller   因为没有空格去区别开这是两个单词，所以两个字符串合成一个字符串，Python会自动认为他是一个单词，那么当然只会将首字母大写啦
```
### 有时候要将一些变量当成字符串才能使程序正常运行，str（）函数就有这样的功能
```python
age = 20
message = "Happy" + age + "rd Birthday!"
print(message)

# 可能你会觉得输出  Happy 23rd birthday! 但真正运行后根本不会打印信息，出现了错误

其实这里面的age类型错误了，Python发现你用了一个值为整数（int）的变量，在上面这样的情况在字符串中使用整数时，需要
特别指出希望python将这个整数当成字符串~
于是需要调用函数str（），这个函数的作用就是让Python将非字符串值表示为字符串

age = 20
message = "Happy" + str(age) + "rd Birthday!"   # 可以用拼接来创建信息，再把整条信息都存储在一个变量中
print(message)

这样就会输出我们想要的了

```
### 在字符串中使用\t或\n来添加空白
```python
print("Python")
print("\tPython")
print("Python\t")

输出的结果为
Python
  Python
Python # 就是在右边添加了空白，看不出来罢了
# \t就相当于tab，即在字符串左边添加了一小段空白
```
```python
print("Languages:\n\tPython\n\tC\n\tJavaScript")

输出结果为
Languages:
  Python
  C
  JavaScript
 
# \n就是换行的作用
```
### 删除字符串的空白
* 方法strip(),rstrip(),lstrip()函数
```python
best_language = " python "
best_language.strip()
print(best_language)

我们会发现输出结果依然是左右带有空格的字符串
# 看来，这种strip方法删除空白只是暂时的，并不是永久性的改变字符串

best_language = " python "
best_language = best_language.strip()      # 要想永久删除字符串中的空白，必须将删除后的结果存回到变量中
print(best_language)

这样就将空白永久清除了

strip()是清空两边
rstrip()是清空右侧
lstrip()是清空左侧
 
 ```
 
 ## 0x3 数字
 * 在Python中，可直接对数字进行四则运算
 ```python
 2 + 3
 3 - 2
 2 * 3 
 3 / 2       # 运行后都会直接的到结果
 
 3 ** 2      # 表示3的2次方
 10 ** 6       # 表示10的6次方
 
 
 2 + 3*4 
 （2 + 3 ）* 4      # 用括号可以改变运算先后顺序
 ```
 
 ## 0x4 注释：#号后面的内容为注释                   
                          
 ## 0x5 Python禅言：输入import this 后执行
 ```python
 
 The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!

```
# 第二章 列表
## 0x0 定义：列表由一系列按特定顺序排列的元素组成，可以将任何东西放入列表中（可以类比c语言中的数组）
* 因为列表通常包含多个元素，所以我们一般为列表定义名字时候用复数的名称是一个不错的选择，eg：names，families,cars,trees....
```python
movies = ["The tinder swindler","Inception"，"Tenet","interstellar"]
print(movies)
print(movies[0])   # 通过指定位置访问列表中元素的方法
print(movies[2])
print(movies[3].title())

输出结果为
["The tinder swindler","Inception"，"Tenet","interstellar"]
The tinder swindler
Tenet
Interstellar



但是有时候列表中的元素非常多的时候，而且并不知道列表长度的情况下，我们想访问最后一个列表元素怎么办呢？
Python很机智，可以将位置定为-1从而来访问列表的最后一个元素（当然想访问倒数第二个第三个，即-2 -3也是可以的~）

print("movies[-1]")
输出结果为
interstellar


```

## 0x2 修改、添加和删除列表元素      
         
### 1. 修改列表元素       

```python


movies = ["The tinder swindler","Inception","Tenet","interstellar"]
print(movies)

movies[0] = "Black Mirror"
print(movies)

输出结果为
['The tinder swindler', 'Inception', 'Tenet', 'interstellar']
['Black Mirror', 'Inception', 'Tenet', 'interstellar']


```

### 2. 添加列表元素
```python
在列表末尾添加元素

movies = ["The tinder swindler","Inception","Tenet","interstellar"]
movies.append("Black Mirror")     # append的意思是‘追加，附加’，这里它的作用就是将元素添加到列表末尾
print(movies)


输出结果为
["The tinder swindler","Inception","Tenet","interstellar","Black Mirror"]






# append的存在让动态地创建列表变得轻而易举。我们生活中通常要在一个列表中不停添加进去新内容，这时append的作用就来了

movies = []
movies.append("The tinder swindler")
movies.append("Inception")
movies.append("Tenet")
movies.append("interstellar")
print(movies)

输出结果为
["The tinder swindler","Inception","Tenet","interstellar"]




```


```python
在列表中插入元素

movies = ["The tinder swindler","Inception","Tenet","interstellar"]
movies.insert(0，"Black Mirror")     # insert译为'嵌入，插入'
print(movies)

输出结果为
['Black Mirror', 'Inception', 'Tenet', 'interstellar']

```

### 3. 删除列表元素
```python
用del语句删除元素


movies = ["The tinder swindler","Inception","Tenet","interstellar"]
del movie[0]
print("movies")

输出结果为
["Inception","Tenet","interstellar"]


```
```python
用pop()方法删除元素


movies = ["The tinder swindler","Inception","Tenet","interstellar"]
print(movies.pop())      # 也可以用popped_movies = movies.pop()把弹出的值赋给变量，然后print(popped_movies)也是一样的效果
print(movies)

输出结果为
interstellar
['The tinder swindler', 'Inception', 'Tenet']


pop()可以删除列表末尾的元素，与其说是删除，pop这个词翻译为'弹出'。列表就像一个栈，最后入栈的是interstellar，所以最先从栈顶弹出的就是interstellar


但其实，pop()可以用来删除任意指定位置的元素，上面那种形容就是为了更好理解它不指定位置时候的删除原理而已。
popped_movies = movies.pop(2)
popped_movies = movies.pop(0)

注意：使用pop()后，被删除的元素就不再存在于列表中了，但与del不同的是，使用pop删除后的元素依然可以被继续额外使用，只不过不在列表中了而已

```
**如果从列表中删除一个元素，且不再以任何方式使用它，就用del；如果在删除元素后还想继续使用这个元素，就用pop**
       
```python
用remove方法删除列表中元素

movies.remove("Tenet")  
# 这种情况是我们不知道这个值在列表中的位置，但我们知道它的实际值，这时就用remove()将它删除
# remove和pop一样，在删除后也可以继续使用

```

## 0x3 列表中元素排序            
### 永久性排序————sort()方法
```python

letters = ["x","a","z","f"]
letters.sort()
print(letters)

输出结果为
['a', 'f', 'x', 'z']

# 永久性的修改了列表顺序，而且sort()是按照字母正向的顺序排序的。


当然还可以按字母逆向的方向排序，只需要向sort()方法传递参数即可，这个信息参数就写在（）中
letters.sort(reverse = True)


输出结果为
['z', 'x', 'f', 'a']

```

### 临时排序————sorted()函数
* 一边要保留元素原来的排序，一边又要以别的排序呈现，就要使用sorted()函数了
```python

letters = ["x","a","z","f"]
print(letters)
print(sorted(letters))
print(sorted(letters,reverse=True))
print(letters)



输出结果为
['x', 'a', 'z', 'f']
['a', 'f', 'x', 'z']
['z', 'x', 'f', 'a']
['x', 'a', 'z', 'f']         # 可见sorted()函数一点都不影响原来的排序

```

### 反转排序————reverse()方法
      
```python


movies.reverse()  # 即可反转现在的排序


注意：虽然说reverse()方法是永久性的改变顺序，但随时可以恢复到原来的顺序啊，因为只要再用一次reverse()即可

```

## 0x4 列表的长度
* 使用函数len()查看列表的长度：列表的长度就是列表所包含的元素的个数         
```python

letters = ["x","a","z","f"]
i = len(letters)            or直接print(len(letters))
print(i)     


输出结果为
4
```

## 0x5 for循环(扫描整个列表)
* 我们用for循环来挨个打印出列表中电影的名字
           
```python


movies = ["The tinder swindler","Inception","Tenet","interstellar"]
for movie in movies:         # 让python从列表movies中取出一个电影存储在变量movie中
    print(movie)
    

输出结果为
The tinder swindler
Inception
Tenet
interstellar



在for循环后，缩进的代码是包含在for循环中的，而不缩进表明出循环
for movie in movies:        
    print(movie)
    print(.....)
print(.....)           # 这行就出了循环

```


## 0x6 创建数值列表
### 函数range()
       
* 函数range()能够生成一系列的数字
```python

for number in range(1,5):
    print(number)
    
    
输出结果为
1
2
3
4
# 我们以为会打印数字1~5，但并没有。这是因为函数range()是从你指定的第一个数开始数，到达你指定的第二个数时停止，所以并不包含第二个数
# 所以使用range()时，要根据实际情况，进行 +1 or -1

```

### 数字列表
* 使用函数list()将range()的结果直接转换为列表，即将range()作为list()的参数，会输出一个数字列表
```python

numbers = list(range(1,6))
print(numbers)

输出结果为
[1, 2, 3, 4, 5]     # 这就叫一个数字列表啦

```
            
            
```python
多样式range()使用

numbers = list(range(2,11,2))     # 从2开始数，然后不断加2，直到达到或超过11时停止
print(numbers)
输出结果为
[2,4,6,8,10]





squares = []
for number in range(1, 11):
    square = number ** 2       # 求每个值的平方
    squares.append(square)

print(squares)
输出结果为
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]

```

* 还可以对数字列表进行简单的统计计算
```python

digits = [1,2,3,4,5,6,7,8,9,0]
print(min(digits))
print(max(digits))
print(sum(digits))
输出结果为
0
9
45

```

## 0x7 处理列表的部分元素————切片
* 创建切片就要明确开始和终止位置，与函数range()的停止规则一样，开始于第一个数，在第二个数时停止不包含第二个数
```python

print(movies[1:3])
print(movies[0:4])
print(movies[:4])
print(movies[1:])

print(movies[:])   # 等同于 print(movies)   等同于将此列表复制了一份(创建了一个包含整个列表的切片)
movies_copy = movies[:]  # 这就是复制列表，复制过后我们可以分别操纵movies和movies_copy列表，它们互不影响      但是若用movies_copy = movies这就不叫复制了，这是赋值！

print(movies[-3:])  # 打印列表中的最后三个





如果要遍历列表中的部分元素，要在for循环中使用切片
for movie in movies[:3]:             # 遍历前三个

```


## 0x8 元组
                       
### 定义：列表适合用于存储会变化的数据集合，而有时候我们需要一些固定不变不可被修改的数据。Python将不能修改的列表称为元组。

```python

numbers = (200,50)
print(numbers[0])
print(numbers[1])
print(numbers)
输出结果为
200
50
(200,50)



与列表一样，也可用for循环去遍历元组中的所有值
for number in numbers:
    print(number)

```

### 虽然不能修改元组的元素，但可以给存储元组的变量赋值，即重新定义整个元组
```python

numbers = (200,50)
numbers = (400,100)
# 这样变更是合理的哦，就相当于给numbers重新赋值了另一个元组，与之前的元组没有关系，我们也没有动之前元组中的元素哦~

```
          
              
# 第四章 字典
       
## 0x0 简单的字典
* 我们来设计一个游戏，里面有许多外星人，那么我们描述这些外星人的各种数值时候就要用到字典，字典存储着外星人的基本信息
```python

alien_0 = {"color":"green","points":"5"}        # 零号外星人的各种信息
print(alien_0["color"])
print(alien_0["points"])
输出结果为
green
5

```

## 0x1 使用字典

* 字典是一种动态结构，可以随时添加信息
```python

alien_0 = {"color":"green","points":"5"}  
print(alien_0)

alien_0["x position"] = 0                 # 在字典中添加的两个新信息
alien_0["y position"] = 25
print(alien_0)

输出结果为
{'color': 'green', 'points': '5'}
{'color': 'green', 'points': '5', 'x position': 0, 'y position': 25}   # 这里发现，我明明先添加的x啊，为什么是y在前面？注意了，信息的排列顺序和添加顺序不一致，因为字典中信息的添加顺序根本不重要，重要的是信息与信息之间的关联关系





我们还可以创建一个空字典，不断往里加入信息
alien_0 = {}

```

## 0x2 修改字典
              
* 现在来假设一个场景，随着游戏的进行，一个外星人从绿色变成了黄色
```python

alien_0 = {"color":"green"}
print("The alien_0 is " + alien_0["color"] + ".")

alien_0["color"] = "yellow"
print("The alien_0 is now " + alien_0["color"] + ".")

输出结果为
The alien_0 is green.
The alien_0 is now yellow.

```
                         
* 用del语句删除字典中的某个信息（永久删除不可使用）`del alien_0["color"]`

## 0x3 字典的不同用法
          
* 前面是存储一个角色的各种信息。但字典也可以用来存储众多对象的同一种信息，例如调查许多人最喜欢的编程语言，用字典来存储调查结果。
```python

best_languages = {"roy":"python","ace":"C","anna":"ruby"}
print("Roy's favorite language is " + 
  best_languages["roy"].title()+
    ".")
输出结果为
Roy's favorite language is Python.
# 这里还演示了如何将较长的print语句分成多行，在适当的地方换行后，要加上一个tab，这样就不会报错了，python会把他们当成正常的一行运行的

```
                        
## 0x4 用for循环和方法items()遍历字典
```python

user_0 = {
  "username": "Nightraid",
  "first" : "Night",
  "last" :  "Raid"  }
  
for key,door in user_0.items():
    print("\nKey: "+key)
    print("Door: "+door)
    
    
输出结果为
Key: username
Door: Nightraid

Key: first
Door: Night

Key: last
Door: Raid

```

* 当不需要使用字典中的值时，我们可以遍历字典中的所有key，这时就要用到方法keys()               
`for sth in xxx.keys()`  将在xxx字典中提取出的所有key存储在sth中，然后再打印一下sth就出来咯  












          






 





