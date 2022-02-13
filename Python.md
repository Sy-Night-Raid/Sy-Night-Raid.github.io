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

## 第一种数据类型———字符串
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
message = "Happy" + str(age) + "rd Birthday!"   # 可以用拼接来创建信息，再把整条信息都存储再一个变量中
print(message)

这样就会输出我们想要的了

```
 





