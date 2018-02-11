# choose
## switch 1
```
#include <stdio.h>
void main()
{   int day,month,year,sum;
    printf("please input year,month,day\n");
    scanf("%d %d %d",&year,&month,&day);
    switch(month)/*先计算某月以前月份的总天数*/
    {
          case 1:sum=0;break;
 case 2:sum=31;break;
 case 3:sum=59;break;
 case 4:sum=90;break;
 case 5:sum=120;break;
 case 6:sum=151;break;
 case 7:sum=181;break;
 case 8:sum=212;break;
 case 9:sum=243;break;
 case 10:sum=273;break;
 case 11:sum=304;break;
 case 12:sum=334;break;
    }
    sum=sum+day;  /*再加上某天的天数*/
     /*判断是不是闰年*/
     if((year%400==0||(year%4==0&&year%100!=0))&&month>2) 
          sum++;
     printf("It is the %dth day.",sum);
}
```

## switch 2
```
//switch实现
#include <stdio.h>
int main( ) { 
    int year;
    float money,rate,total; /* 本金 月利率 本利合计*/
    printf("Input money and year =?");
    scanf("%f  %d", &money, &year);/* 输入本金和年 */
    switch(year)
    {
    case 1:
        rate=0.0032;  /* 根据年限定利率 */
        break;
    case 2:
        rate=0.0041;
        break;
    case 3:
        rate=0.005;
        break;
    case 5:
        rate=0.0055;
        break;
    case 8:
        rate=0.0065;
        break;
    default:
        rate=0.0;
    }
    total = money + money * rate *12 * year;
    printf(" Total = %.2f\n", total);
}
```

# for 1
```
//for循环实现
#include<stdio.h>
int main(void)
{
    int count=0,x,y;
    for(x=1;x<35;++x)
    {
        for(y =1; y <35;++y)
        {
            if(((x+y)==35)&&((2*x+4*y)==94))
                printf("鸡：%d， 兔：%d\n", x, y);
            //count++;
        }
    }
    //printf("%d\n", count);
    return 0;
}
```

# for 2
```
#include <stdio.h>
 int main( )
 { int j;   long n;
   printf("Please input number:");
   scanf("%ld", &n);
   for (j=999; j>=100; j--)
   if ( n%j==0 )    /* 若能够整除j，则j是约数 */
      {  printf("3 digits in %ld=%d\n", n, j );
           break;                   /* 控制退出循环 */
    }
   return 0;
 }
 ```
 
 # for 3
 ```
   #include <stdio.h>
 main()
{   int i=1,x,y,a=1;
    printf("Input X and Y:");
    scanf("%d%d",&x,&y);
    while (i<=y)
    {a=a*x%1000;
     i++;
    }
  printf("3 digits is:");
  printf("%d\n",a%1000);
}
```

# for 4
```
main( )
{ char c='z';
  int i,j,n;
  printf("\nPlease Enter n:");
  scanf("%d",&n);
  for(i=1;i<=n;i++) //控制输出行数
   {  //打印最后一个字符之前的空格和字符
    for(j=1;j<=n+i-2;j++)
       if(j==n-i+1)  printf("%c",c--);
       else  printf(" ");
    printf("%c\n",c--);   //打印最后一个字符
   }
  for(i=1;i<n;i++)
   {  for(j=1;j<=2*(n-1)-i;j++)
         if(j==i+1)  printf("%c",c--);
         else  printf(" ");
      printf("%c\n",c--);
   }
}
```
