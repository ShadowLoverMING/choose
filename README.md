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
