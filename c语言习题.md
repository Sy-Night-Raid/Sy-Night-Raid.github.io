# 第一部分 基础篇        
      
## 0x0 基本库函数的使用
* 问题描述：编制100以内两个整数（随机产生）的加法运算练习程序
* ```    
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













