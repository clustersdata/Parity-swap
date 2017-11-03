# Parity-swap

Parity swap

Problem Description

给定一个长度为偶数位的0,1字符串，请编程实现串的奇偶位互换。

Input

输入包含多组测试数据；

输入的第一行是一个整数C，表示有C测试数据；

接下来是C组测试数据，每组数据输入均为0,1字符串，保证串长为偶数位(串长<=50)。

Output

请为每组测试数据输出奇偶位互换后的结果；

每组输出占一行。

Sample Input

2 0110 1100

Sample Output

1001 1100

代码：

#include<string.h>

#include<stdio.h>

int main()

{
    int n,i;
    
    char s[100],temp;
    
	scanf("%d",&n);
  
    while(n--)
    
    {
    
        scanf("%s",s);
        
        for(i=0;i<strlen(s);i+=2)
        
        {
        
            temp=s[i];
            
            s[i]=s[i+1];
            
            s[i+1]=temp;
            
        }
        
        for(i=0;i<strlen(s);i++)
        
          printf("%c",s[i]);
          
        printf("\n");
        
    }
    
    return 0;
    
}
