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
