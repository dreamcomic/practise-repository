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



//以字节为存储单位基础上
//大端储存模式，是指数据的低位保存在内存的高地址中，而数据的高位存在内存的低地址中
//小端存储模式，数据高位存内存高地址，数据低位存内存的低地址。
#include <stdio.h>
#include <stdlib.h>
//求一个机器是大端还是小端储存，可以用下面的操作。
//原理char只有一个字节，而char*是有一个字节，而int有四个字节
//如果int存的1是小端储存模式，那么1一定存在前面的地址
//我们知道int地址占4个字节，小端的话那么在第一个字节里面0x01就是1
//所以如果是小端储存就一定能打印出1.

//这里的大小端储存要和前面的栈里的变量储存区分开，变量储存是整个变量的地址
//而这里是变量地址内部的地址。
// int main()
// {
//     int a = 1;
//     //00000000000000000000000000000001//正数三码相同
//     char* p = (char *)&a;
//     //这里*P存的地址就一定是a所占内存的第一个字节
//     printf("%3d\n",*p);//打印结果是1说明是小端存储
//     //这里打印结果为1，说明其中存储了补码为00000001，而打印出对应的结果，说明是小端储存，低位，在低地址上
//     system("pause");
//     return 0;
// }


//c语言中普遍存在整形提升，如短整型和整形相加，char型和整形相加
//打印时的char和short类型等等
//整形提升
// int main()
// {
//     char a = -1;
//     //11111111111111111111111111111111   这就是-1的补码，但是这里是32个bit位8个字节
//     //11111111      而char只有8个bit位，所以这里只能存的是8个1，并且char也是有符号位的，所以这里第一个仍然是符号位
//     int c = a;
//     //那么这里再赋值给整形数c的时候就需要进行整形提升，因为char是有符号位
//     //11111111111111111111111111111111所以这里按照符号位的数来提升
//     //在进行操作，结果仍然是-1.
//     unsigned char b = -1;
//     //11111111111111111111111111111111   这是-1的补码
//     //11111111//一样的截断得到8位
//     //而这里unsigned就是无符号位数字，相当于也就整数，所以源码反码补码相同
//     int d = b;//所以这里b在进行整形提升的时候的补码是00000000000000000000000011111111
//     //一样的减一按位取反得到原码。因为符号位是0，所以整数不改变d就是255
//     printf("%d\n", c);
//     printf("%d\n", d);
//     system("pause");
//     return 0;
// }

// int main()
// {
//     char a = 128;//打印发现128和-128结果一样，原因就是char只有8个bit位存储的数字最大不过127或者-127
//     //原因是整形截断的时，前面的符号位被砍掉了
//     //先进性整形截断
//     //10000000000000000000000010000000原码
//     //01111111111111111111111101111111反码
//     //01111111111111111111111110000000补码
//     //10000000；a所储存的就是这个
//     //那么再打印的时候要进行整形提升
//     //11111111111111111111111110000000得到补码
//     //那么得到就是a整形提升之后数字的补码，但是我们知道需要打印的是无符号数字
//     //那么三码相同
//     printf("%u\n", a);//%u打印无符号数字
//     system("pause");
//     return 0;
// }

// int main()
// {
//     int a = -20;
//     //10000000000000000000000000010100
//     //11111111111111111111111111101011
//     //11111111111111111111111111101100

//     unsigned int b = 10;
//     //00000000000000000000000000001010
//     //11111111111111111111111111101210二者补码之和
//     //11111111111111111111111111110010
//     //11111111111111111111111111110001
//     //00000000000000000000000000001110
//     printf("%d\n", a + b);
//     system("pause");
//     return 0;
// }
#include <string.h>
// int main()
// {
//     char a[1000];
//     char c = 128;
//     int b = -1;
//     for(b = 0;b < 1000; b++)
//     {
//         a[b] = -1 - b;
//     }
//     printf("%d\n", strlen(a));//\0的ASCII码值是0转换位二进制就是000000000，所以当a[b]的二进制的值为00000000即是得到的\0,因为字符在内存里面存的相当于就是ASCII值，整形
//     //而其是无符号数，故而补码是000000000；再接着计算从111111111到00000000那么相减即可
//     printf("%d\n", c);
//     system("pause");
//     return 0;
// }


// int main()
// {
//     printf("%c\n", 99);//从这里的打印结果就可以看出，我们的打印的时候是转换为ASCII码值去打印的
//     char a[3] = {98,98,0};
//     printf("%s\n", a);//我们这里也可以看出，实际上字符串比较的是字符串里面的ASCII值
//     printf("%d\n", strlen(a));//包括字符串的一系列函数，都是对字符串所转换出的ASCII值比较，这里也解释为什么char类型认为也是整形家族
//     printf("%d\n", sizeof(a));
//     system("pause");
//     return 0;
// }

// int main()
// {
//     float a = 1E2;//这里的1E2表示就是1.0*10的2次方。也就是常见的科学计数法。
//     printf("%lf", a);
//     system("pause");
//     return 0;
// }

// int main()
// {
//     int a = 9;
//     float *p = (float *)&a;
//     printf("%d\n", a);
//     printf("%f\n", *p);
//     *p = 9.0;
//     printf("%d\n", a);
//     printf("%f\n", *p);
//     system("pause");
//     return 0;
// }




//浮点数的储存方式。IEEE74规定所有的而二进制浮点数都可以表示为
//(-1) * s *M * 2*E
//float是32个bit位，据规定
//第一个bit位存s，第2个到第9个存E（且认为E是无符号数），第10个到32个存M。
//double float 类似
//第1个bit位存s，第2个到第12个存E（且认为E是无符号数），第13到64位存M
//s存0即是整数，存1则是负数
//M由于总是表示为[1,2),所以就不存储1，只存储后面的有效数字
//E由于存储时，E可以是负数，那么为了有负数，就是E在存储的时候先+127（64bit就+1023）存进内存，拿出来算的时候减去127。
//


#include <stdio.h>
#include <stdlib.h>

// enum car {height ,weight ,width ,lenth};
//在没有认为定义枚举变量时，第一个枚举变量会是0，往后一次加一
// int main()
// {
//     int a = height, b = weight;
//     printf("%d, %d ", a, b);//由上述，这里打印的就是0，1
//     system("pause");
//     return 0;
// }

enum car {height = 11,weight ,width = 10,lenth} tool;
//如果下一个变量未定义，，那么就是前一个变量加一
//此外枚举变量在赋值的时候必须要强制类型转换，而且枚举变量一般都是整形类型的数据
//但是相当于被强制类型转换的类型，所以在给枚举变量符赋值时应该用整形并且要强制类型转换
enum leg {hi = 10,widt, v, enu} person;
int main()
{
    int a = height, b = weight , c = width, d = lenth;
    tool = (enum car)9;//对美剧变量的定义，这里定义的枚举变量时定义的tool，而在一开始{}里面的变量定义的时常量，即不可再改变，可以拿去赋值
    a = height, b = weight , c = width, d = lenth;
    if(tool >= person)
    printf("%d, %d ,%d, %d \n", height, b, c, d);//由上述，
    system("pause");
    return 0;
}



#include <stdio.h>
#include <stdlib.h>
#include <string.h>
// void  strreverse(char * const a)
// {
//     int ri = strlen(a) - 1;
//     int le  = 0;
//     for(;le < ri;le++,ri--)
//     {
//         char tem = a[le];
//         a[le] = a[ri];
//         a[ri] = tem;
//     }
// }
// int main()
// {
//     char a[] = "abcdefghij";
//     strreverse(a);
//     printf("%s\n", a);
//     system("pause");
//     return 0;
// }

// int main()
// {
//     char arr[22] = "********** **********";
//     int mid = (strlen(arr) - 1)/2;
//     int d = 0;
//     for(d = 0;d < 10; d++)
//     {
//         arr[mid + d] = ' ';
//         arr[mid - d] = ' ';
//         printf("%s\n", arr);
//     }
//     for(;d > 0;d--)
//     {
//         arr[mid + d] = '*';
//         arr[mid - d] = '*';
//         printf("%s\n", arr);

//     }
//     system("pause");
//     return 0;
// }/

// int caculate(int const a)
// {
//     int temp = a;
//     int bottle = a;
//     int remainder;
//     for(;temp > 1;)//temp是代表空瓶子数
//     {
        
//         if(temp % 2 == 0)
//         {
//             temp = temp/2;
//         }
//         else if(temp != 1&& temp%2==1)
//         {
//             temp = (temp - 1)/2;
//             remainder++;//非偶数的空瓶数算上上
//         }
//         bottle += temp;//这里算上的喝的饮料瓶数
//         if(remainder!=0)
//         {
//             temp += remainder;
//             remainder =0;
//         }//这里把完整的空瓶数算出来
//     }
//     return bottle;
// }

// int main()
// {
//     int a;
//     scanf("%d", &a);
//     printf("%d\n",caculate(a));
//     system("pause");
//     return 0;
// }
#include <time.h>

// void iniarr(int * arr, int sz)
// {
//     int c;
//     for(c = 0;c <= sz - 1; c++)//sz数组个数，得到下标需减一
//     {
//         arr[c] = rand();//给数组随机赋值
//     }
// }

// void sortarr(int *arr, int sz)
// {
//     int ri = sz - 1;//最右边个元素的下标
//     int le = 0;
//     int a = 0;//第几个判断元素
//     for(;a <= sz;a++)
//     {
//         if(arr[a]%2==1)
//         {
//             int tem = arr[a];
//             arr[a] = arr[le];
//             arr[le] = tem;
//             le++;
//         }//交换元素，并且讲le++把0下标腾出来
//         if(arr[a]%2 == 0)
//         {
//             int tem = arr[a];
//             arr[a] = arr[ri];
//             arr[ri] = tem;
//             ri--;
//         }
//     }
// }

// void print(int *arr, int sz)
// {
//     for(int c = 0;c <= sz - 1;c++)
//     {
//         printf("%6d",arr[c]);
//     }
// }
// int main()
// {
//     srand((unsigned int)time(NULL));
//     int arr[10];//数组
//     int sz = sizeof(arr)/sizeof(arr[0]);//得到元素个数
//     iniarr(arr,sz);
//     sortarr(arr,sz);
//     print(arr,sz);
//     system("pause");
//     return 0;
// }

// int main()
// {
//     char a[] = "I am a pig";
//     char b[] = "0000000000";
//     // system("shutdown -s -t 60");
//     scanf("%[^\n]",&b);
//     if(strcmp(a,b)==0)
//     {
//         system("shutdown -a");
//     }
//     system("pause");
//     return 0;
// }






