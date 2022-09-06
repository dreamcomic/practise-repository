# practise-repository
初学者的使用
// #include <stdio.h>
// #include <stdlib.h>
// int main()
// {   
//     int a = 1;
//     while(a<=10)
//     {   
//         if(5==a)
//             continue;//这里continue需要注意是；continue回到的是while下一次循环的判断部分。
//         printf("%d\n", a);
//         a++;
//         break;//而break就是终止循环.
//     }
//     system("pause");
//     return 0;
// }





// #include <stdio.h>
// #include <stdlib.h>
// int add(int x)
// {   
//     static int z = 0;
//     z = x+1;
//     printf("z = %d\n", z);
//     return z;
// }
// int main()
// {
//     int b = 0;
//     while(b<=100)
//     {
//         if(b%2!=0)
//             printf("奇数 = %d\n", b);
//         b = add(b);
//     }
//     system("pause");
//     return 0;
// }
// int add(int x)
// {   static int z = 0;
//     z = x +2;
//     return z;
// }
// int main()
// {   
//     int a = -1;
//     while(a<=98)
//     {   
//         a = add(a);
//         printf("a = %d\n", a);
//     }
//     system("pause");
//     return 0;
// }



//int main()
// {   int a = 43;
//     if(5 == a)//这里这的注意的是==才是判断是否相等。而=是赋值。所以为了防止这种错误，把常量放在前面如此，这样可以避免错误。
//     {   
//         printf("meet angel\n");
//     }
//     system("pause");
//     return 0;
// }
// {   int a = 11;
//     int b = 99;
//     if(a>=100)
//     {   if(a<b)
//         printf("%d\n", a);
//     }
//     else//这里的else就是对应的上面个if。
//     printf("%d\n", b);
//     system("pause");
//     return 0;

// }
// {   
//     int a= 92;
//     int b = 99;
//     if(a>=1000)  
//         if(b<a)
//         printf("%d\n", a);
//         else
//             printf("%d\n", b);//这里的else对应的是与其更近的那个if。如果想这个else对应上面的if。则加一个{}在第一if后面，把第二个if包含于其中。
//     system("pause");
//     return 0;

// }
// if(the expression)
//     the sentence;//如果表达式结果为真，执行语句；否则什么都不执行。
// if(the exorssion)
//     the sentence;
// else
//     the sentence2;//如果表达式结果为真，执行语句1；否则执行语句2。
// if(expression)//如果表达式为真，则执行语句1；否则判断下一个表达式。
//     the first sentence;
// else if(the second expression)
//     the second sentence;//如果表达式2为真，执行表达式2，否则执行表达式3.
// else   
//     the third sentence;
// int main()
// {   
//     int age = 16;
//     if(age>=28)
//         printf("the middle people or you are the old.");//要执行多条语句可以用代码块。
//     else
//     {   
//         if(age>=18)
//             printf("Adult.\n");
//         else if(age<18 && age>12)
//             printf("teenager\n");
//         else if(age<12)
//             printf("child.\n");
//     }
//     system("pause");
//     return 0;
//}
//     if(age>=18)
//         printf("you are adult.\n");
        
//     else if(age>12)
//         printf("you are teenager.\n");
//     else    
//         printf("you are child.\n");
//     system("pause");
//     return 0;
//



The second fay:
#include <stdio.h>
#include <stdlib.h>
 int main()
 {   
     char a = 'b';
     char password[20] = {0};
     printf("input your password:\n");
     scanf("%s\n", password);//scanf扫描输出之后敲的回车键，会于输出缓冲区留下\n.而如果在%s后使用了\n，则会导致下一次输入非空白字符才能结束，而这下一次输入会留在缓冲区。
     getchar();//为了清楚上次残留的\n,这里多用一个getchar吸收掉\n来避免后续进入下一个getchar。
     printf("please confirm your password(y/n):\n");
     a = getchar();
     if('y'== a)
     {  
        printf("succes\n");
     }
     else
     {  
        printf("give up\n");
     }
     system("pause");
     return 0;

 }这段代码运行时，如果输入空格键，scanf只会读取空格以前的东西。而下一个来的，就只会读取空格。


the third day（scanf与缓冲区）
#include <stdio.h>
#include <stdlib.h>
int main()
{  int a =1;
   char c = '1';
   char password[10] = {0};
   printf("input your password:\n");
   scanf("%s", password);
   while((c=getchar())!='\n');    //经过实验发现:这里while后面，要加隔断性语句或字符。如这里while后面就该有；。但是由于{}有表示隔断的作用，所以{}后面不再加分号。所以这里用空的{}也可以。
   printf("please confirm your password");
   a = getchar();
   if('y'==a)
   {  
      printf("succeed creating your account");
   }
   else
   {  
      printf("give up your password");
   }
   system("pause");
   return 0;

}


#include <stdio.h>
#include <stdlib.h>
int main()
{   
    int y1, j1, f1, y2, j2, f2=1;
    int y, j, f = 2;
    int shiftj = 0;
    int shifty = 0;
    float ss = 0.000000;
    scanf("%d %d %d", &y1, &j1, &f1);
    scanf("%d %d %d", &y2, &j2, &f2);
    f = f1 + f2;
    if(f>=10)
    {   
        f = f -10;
        shiftj = 1;
    }    
    j = j1 + j2 + shiftj;
    if(j>=10)
    {   
        j = j-10;
        shifty = 1;
    }
    y = y1 +y2 + shifty;
    ss = y + j/10.0 +f/100.0;
    printf("%f\n", ss);
    system("pause");
    return 0;
}



#include <stdio.h>
#include <stdlib.h>
int main()
{   char ch = 'a';
    while((ch = getchar())!= EOF)
    {   
        if(ch < '0' || ch>'9')
            continue;
            putchar(ch);
    }
    system("pause");
    return 0;
}


//for循环
//for(exp1; exp2; exp:3)
//exp1是初始化部分用于初始化循环变量的。exp2时判断部分，用于判断循环时候的终止。表exp3为调整部分，用于循环条件的调整。
#include <stdio.h>
#include <stdlib.h>
int main()
{   
    int a = 0;
    for(a = 1; a<=100; a+=2)//for循环从exp1开始，到达exp2
    {   
        printf("%d\n", a);  //从exp2到{}。
        a++;                //执行完{}到exp3。
    }                       //再次返回exp2。
    system("pause");
    return 0;
}

//for循环中的break与continue
#include <stdio.h>
#include <stdlib.h>
int main()
{   int a = 0;
    for(a = 1;a <=100; a+=1)
    {   
        printf("a = %d\n", a);
        if(a>=10)
        {   
            a+=90;
            printf("b = %d\n", a);
            break;  //这里的break一样是跳出循环。
        }
        else         
            continue;//continue回到的是exp3；
    }
    system("pause");
    return 0;
}


#include <stdio.h>
#include <stdlib.h>
int main()
{   
    int i =0;
    int k =1;
    for(i=0; 0==k;i++,k++)//这里如果写成k=0，就会使判断恒为假，而无法循环
    k++;
    printf("k = %d ", k);
    system("pause");
    return 0;
}


4th september


#include <stdio.h>
#include <stdlib.h>
int main()
{   
    int a = 1;
    int b = 1;
    int e = 0;//这里值得我们注意的是变量的作用域。
    for(b = 1; b<=3; b++)
    {
        int c = 1;
    for(a = 1,c = 1; a<b+1;a++)
    {        c = c*a;
    }
            e = e + c;
        if(3==b)
        {   
            printf("%d\n", e);
        }
    }
    system("pause");
    return 0;
}


#include <stdio.h>//switch语句中的switch（）中的括号必须是整形。
#include <stdlib.h>
#include <string.h>
int main()
{   int a =0;
    char password[20] = {0};
    for(a = 0; a<3;a++)
    {   
        printf("in put your password:\n");
        scanf("%s",password );
        if(strcmp(password, "123456") ==0)//C语言中字符串的相等必须要通过转换为strcmp函数来比较。
        {   
            printf("succeed logining\n");
            break;
        }
    } 
    if(3==a)
    {   
        printf("The number of your wrong password is three,please wait try tomorrow.");
    }
    system("pause");
    return 0;

}




#include <stdlib.h>
#include <stdio.h>
int a ;  int b;  int c;//这是全局变量给与函数多个输出值。只要定义的是函数之外的。
int la()
{   
    if(a<b)
    {   
        int d = 0;
        d = a;
        a = b;
        b = d;
    }
    if(a<c)
    {   
        int d = 0;
        d = a;
        a = c;
        c = d;
    }
    if(b<c)
    {   
        int d = 0;
        d = b;
        b = c;
        c = d;
    }

}
int main()
{   
    scanf("%d%d%d",&a, &b, &c);
    la();
    printf("%d>%d>%d", a, b, c);
    system("pasue");
    return 0;
}








