# 第一部分 基础篇        
      
## 0x0 基本库函数的使用
* 问题描述：编制100以内两个整数（随机产生）的加法运算练习程序

```c
#include<stdio.h>                 
#include<stdlib.h>                         
int main()                     
{                           
	int  a,b,c,x=0;  // 本题是计算100以内两个数的和，所以至少要定义三个int型变量a，b，c，分别表示加数，被加数，和       
	a=rand()%100;     // 随机数函数rand（）原型在‘stdlib.h’文件中           
	b=rand()%100;      // 每调用一次rand（） ，便产生一个0~32767之间的随机数，所以如果想要一个0~99之间的随机数，就要用rand（）%100就得到啦       
	printf("\n%d+%d=",a,b);           
	scanf("%d",&c);          
	if(c==a+b){              
		printf("The answer is right!\n");               
	}               
	else {              
		printf("The answer is wrong!\n");             
		printf("The right answer is %d+%d=%d\n",a,b,a+b);              
	}                
	return 0;                  
	
}                 
```
            
## 0x1 基本数据类型的使用
* 问题描述：编写一个程序，当输入小写字母时，程序能自动转换为大写字母；当输入大写字母时，程序能自动转换为小写字母；当输入非字母时，不进行任何转换；当输入非字母“#”时，程序结束。
```c
#include<stdio.h>
int main()
{
	char c;
	do{
		scanf("%c",&c);
		if(c>='a'&&c<='z'){
			printf("%c",c-32);
		}
		else if(c>='A'&&c<='Z'){
			printf("%c",c+32);
		}
	}while(c!='#');   //注意这个#也是符号，只要是符号就必须包裹在'中' 
	return 0;
	
 } 
 /* 1.我们运行了一下，发现很有趣哦我输单个字母s会出来大写字母S，我们输入wofer会出来大写WOFER，不管你输入多少字母都能一次性转换；直到输入#会终止程序 
  2.有趣的一点是虽然我们scanf（）输入的是字符类型%c，但如果我们把printf中改成%d，则会出现我们输入s出来一个数的情况，很有趣，因为在内存中
  字符型数据是以ASCII码存储的，所以c语言中字符数据char和整型int之间可以通用。一个字符数据既可以以字符形式输出，也可以以整数形式输出
  3.以字符形式输出时，需要先将存储单元中的ASCII码转换成相应字符，然后输出。以整数形式输出时，直接将ASCII码作为整数输出 
  4.也可以对字符数据惊醒算术运算，此时相当于对它们的ASCII码进行算术运算
  ！！！！说白了，字符数据的根本就是数字 */ 

```         
```c
#include<stdio.h>
int main()
{
	char c;
	while(c!='#'){
		 	scanf("%c",&c);
		if(c>='a'&&c<='z'){
			printf("%c",c-32);
		}
		else if(c>='A'&&c<='Z'){
			printf("%c",c+32);
		}
	}
	return 0; 
	

	
 } 
 //在此题中，while和do while没有任何区别，用谁都可以
```
            
## 0x1.1 思考问题
* 问题描述：对字母加密的问题，如将China译成密码，其加密规律为：用原来字母后面的第4个字母代替原来的字母，例如字母A后面第4个字母是E，用E代替A。因此，China应译为Glmre
```c


```













