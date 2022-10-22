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



#include <stdio.h>
#include <stdlib.h>
#include <time.h>
// // int main()
// // {
// //     unsigned char a = 200;//无符号数整形提升的时候，直接补充0；有符号位数整形提升的时候根据符号位补充
// //     unsigned char b = 100;
// //     unsigned char c = a + b;//所以这里自然得出二者结果的和是300，
// //     //但是，又要进行整型截断，我们知道256就在第9位，那么也就是说300-256就是胜在后八位的数字，也就是44，即c是44
// //     printf("%d %d",a + b, c);//因为是打印整形，那么 a + b 就要进行整形提升。计算后结果依然也是300.因为unsigned的数原码补码反码相同
// //     system("pause");
// //     return 0;
// // }
// //大端储存，小端储存。//高地址存低位数，大端。低地址存低位数，小端。
// //一个整型4个字节，那么一个存16（转换位16进制就是00 00 00 10）那么小端储存的时候，这个10可能存在第一个字节。
// //大端储存的时候存在第4个字节

// // void initialarr(int  (*arr)[col])//这里是对于二维数组的定义的少有办法。其实就是利用对二维数组的定义，实际相当于先存一行的数组，再把那个数组作为元素存进数组。
// // {
// //     for(int a = 0;a <= col ;a ++)
// //     {
// //         arr[0][a] = 1;
// //     }
// // }
// int main()
// {
//     int arr[][5] = {};//这里定义成功，我们可以这么理解，机器在理解的时候，先理解arr[],就是正常的定义了一个数组，可以不定义个数
//     //但是当再定义一次的时候，就相当于把后面的数组当元素去定义了，那么元素是什么格式（占多少内存），就应该是确定的，就像一般定义的是整形数组
//     //数组大小都是确定的。那么再定义好之后，在定义这个数组里面类型的元素。者也就是理解的顺序。那么我们就会发现，其实arr存的地址，其实是
//     //前面五个元素的组成数组的地址。这也就牵扯出二维数组的第二种定义。int (*arr)[]，注意括号不可以少，因为结合性的原因。
//     //类比的，三维思维数组也是效果相似
//     // initialarr(arr);
//     system("pause");
//     return 0;
// }

#define row 11
#define col 11


//杨辉三角

// void str(int (*arr)[col])
// {
//     int r = 0, c = 0;
//     for(;r <= row; r++)
//     {
//         for(c = 0;c <= col;c++)
//         {
//             arr[r][c] = 0;
//         }
//     }
// }
// void intialstr(int arr[row][col])
// {
//     for(int i = 0;i <= col; i++)
//     {
//         arr[0][i] = 0;
//         if(i == (col - 1)/2)
//         {
//             arr[0][i] = 1;
//         }
//     }
// }


// void print1(int arr[row][col])
// {
//     int r ,c;
//     for(r = 0; r <= row - 1; r++)
//     {
//         for(c = 0; c <=col - 1; c++)
//         {
//             if(arr[r][c] != 0)
//             printf("  %4d  ",arr[r][c] );
//             else
//             printf("        ");
//         }
//         printf("\n");
//     }
// }
// void setstr(int (*arr)[col])
// {
//     int r = 1, c = 0;
//     for(;r <= row; r++)
//     {
//         for(c = 0;c <= col;c++)
//         {
//             if(c < (col - 1)/2)
//             arr[r][c] = arr[r - 1][c] + arr[r - 1][c + 1];
//             if(c > (col - 1)/2)
//             arr[r][c] = arr[r - 1][c] + arr[r - 1][c - 1];
//             if(c ==(col - 1)/2&& r%2 == 0 )
//             {
//                 if(arr[r - 1][c - 1] == 0)
//                 {
//                     arr[r][c] = 1;
//                 }
//                 else{
//                     arr[r][c] = arr[r - 1][c + 1] + arr[r - 1][c - 1];
//                 }
//             }
//         }
//     }
// }

// int main()
// {
//     int arr[row][col];
//     str(arr);
//     intialstr(arr);
//     setstr(arr);
//     print1(arr);
//     system("pause");
//     return 0;
// }
//失败品杨辉三角。
//上述失败的原因是没有去解析杨辉三角的数学规律。可以考虑先把边缘的1打印出来，在进行相加，就能得到斜的杨辉三角


// void initialstr(int (*arr)[col])
// {
//     int r, c;
//     for(r = c = 0;r <= row - 1; r++)//11行11列的数进行初始化
//     {
//         for(c = 0;c <= col - 1; c++)
//         {
//             arr[r][c] = 0;
//         }
//     }
// }

// void print(int (*arr)[col])
// {
//     int r,c;
//     for(r = c = 0;r <= row - 1; r++)
//     {
//         for(c = 0;c <= col - 1; c++)
//         {
//             if(arr[r][c] != 0)
//             {
//                 printf("%d ",arr[r][c]);
//             }
//             else if(arr[r][c]==0)
//             {
//                 printf("  ");
//             }
//         }
//         printf("\n");
//     }
// }

// void setarr1(int (*arr)[col])
// {
//     int r,c;
//     for(r = 0;r <= row - 2;r++)//只对10行进行打印，这样避免对指针的越界访问
//     {
//         for(c = 0;c <= col - 2;c++)//同样只对10列进行打印避免越界访问
//         {
//             if(c == 0)
//             {
//                 arr[r][c] = 1;
//             }
//             if(r==c)
//             {
//                 arr[r][c] = 1;
//             }
//         }
//     }
// }
// int main()
// {
//     int arr[row][col];
//     initialstr(arr);
//     setarr1(arr);
//     print(arr);
//     system("pause");
//     return 0;
// }


//计算机实现排除逻辑算法

// void exclude(int a, int c)//a信息条数，c信息的假的数量。得出结果，谁的信息可能是假的
// {
//     scanf("%d%d", a ,c);
//     int killer = 1;//这里设四个人分别是1234.他们的表述
//     for(;killer <= a;killer++)
//     {
//         static int ci = 0;
//         int result;//讲每个人的陈述输入，获得result即可·
//         if( (result) >= a - c)
//         {
//             ci ++;
//             printf(" the %d result %d\n",ci, killer);
//         }
//     }
// }

// int main()
// {

//     system("pause");
//     return 0;
// }//用上述逻辑算法，可以给出对应的排除结果，对于某些推理很好用。比如一千人的答案
#include <time.h>

// void initial(int * arr)
// {
//     for(int i = 0; i <= 36; i++)
//     {
//         arr[i] = rand()/37;
//     }
// }

// void judge(int arr[])
// {
//     for(int a = 0;a < 6;a++)
//     {
//         if(arr[a] > arr[a + 1])
//         {
//             int tem = arr[a];
//             arr[a] = arr[a+1];
//             arr[a+1] = tem;
//         }
//     }
// }
// int main()
// {
//     int arr[36];
//     srand((unsigned int)time(NULL));
//     initial(arr);
//     judge(arr);
//     system("pause");
//     return 0;
// }
//赛马36匹马，6个赛道，得出前三名，最少要几次。
//跑6次，分6组，6组第一名去比赛，对应名次分组。把第一组的前三名，第二组的前二名，第三组的第一名。一共八次。

// int main()
// {
    
// }
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


#include "commomuse.h"

// void levorotation(char *arr)//镜像右旋函数。如ABCDE->EDABC将旋转元素与之前位置形成镜像对称
// {
//     int ri = strlen(arr) - 1;//最右边元素的下标
//     int le = 0;
//     int num;//镜像右旋字符个数。
//     scanf("%d", &num);
//     for(int time = 0;time < num ;time++)//右旋次数
//     {
//         char tem = arr[ri];//先临时存储这个最右边字符
//         for(int v = 0;v < ri - time;v++)//当右旋最左边个字符，
//         {
//             arr[ri - v] = arr[ri - v - 1];//移动字符
//         }
//         arr[le + time] = tem;//将最右边的字符放入该有的位置

//     }
// }

// void judgestr(char *arr,char*arr1)//判断字符串是否相等
// {
//     if(strcmp(arr,arr1)==0)
//     {
//         printf("yes");
//     }
// }
// int main()
// {
//     char arr [] = "ABCDE";
//     char arr1 [] = "EABCD";
//     levorotation(arr);
//     printf("%s\n", arr);
//     judgestr(arr, arr1);
//     system("pause");
//     return 0;
// }

//递增型矩阵函数
//1.先对行用折半查找。在找的时候注意留下两行。实现时，将le < ri - 1即可。如3，5，这样所得结果才是两行->就变成3，4，注意比较所得两行是否与其相等
#include <stdio.h>
#include <stdlib.h>
#include <time.h>
#include <windows.h>
#include <string.h>
#include <math.h>
#include <malloc.h>
void initial(int *arr,int get1, int get2);
void print(int *p,int sz);
void judge(int *p,int get1, int get2);
void printresult(int *arr, int *p, int sz);

#include "commonuse.h"

void initial(int *p,int get1, int get2)
{
    int le = 0,sz = get2 - get1 + 1;//数组个数sz
    for(;le <=sz - 1;le++,get1++)//sz-1才是最右边下标的元素
    {
        p[le] = get1;
    }

}
void print(int *p,int sz)
{
    int le = 0;
    for(;le <=sz - 1;le++)//sz-1才是最右边下标的元素
    {
        printf("%4d", p[le]);
    }
}

void judge(int *p,int const get1, int const get2)
{
    int tem = 0;//暂时储存我们的每位数相乘的答案。
    int Tem = 1;//暂时存储我们的每次迭代结果
    
    for(int a = 0;a <= get2 -  get1;a++)//对每个数进行筛查的循环
    {
        Tem = p[a];
        int value = 1;//value表示临时数组里面存储的元素个数
        int attch = 0;//表示依附幸福数的个数
        for(;Tem > 0;Tem  = tem)//这个循环算出最终是否是独立幸福数
        {
            
            int arr[value];//创建动态数组//c语言里面居然有，早知道前面直接就创建动态数组了。
            arr[value - 1] = Tem; //将算出来的数存入临时数组进行比较，第一个数据也要储存。
            for(tem = 0;Tem > 0;Tem /= 10)//这个循环算出一次迭代的值
            {
                tem += pow((Tem%10),2);//计算平方
            }
            attch--;//用此来标记有多少依附性幸福数,这里把1也算进去
            for(int le = 0;le <= get2 -get1;le++)
            {
                if(p[le]==tem)
                {
                    p[le] = 0;
                }
            }//以这种方法筛掉依附性幸福数，同时是筛选掉一部分依附非幸福数的的数，依此法，可以保证前面某些数即使被认定为幸福数，后续便于筛查出特立
            for(int c = 0;c <= value - 1;c++)//这个循环用于检查一个数是否为死循环
                {
                    if(arr[c] == tem && tem != 1)
                    {
                        p[a] = 0;
                        tem = 0;//使tem等于0，那么在开始的时候自然就会停下循环
                        break;
                    }
                }//如此就判断出非幸福数，同时也把依附性幸福数排除掉。
            if(tem == 1)//说明是循环数
            {
                p[a] =  attch;//因为前面把1也算如依附幸福数，所以在后面算依附性应该要除掉一个数
                break;//得到1说明是幸福数，跳出循环。
            }
            value++;//如果这里完成一次之后，那就对value需检测元素加一
        }
    }
    
}//这里将数组里面每个数字给换成0或者负数，负数说明是独立性幸福数，将独立性幸福数负数绝对值减一就是其依附性幸福数个数。

void printresult(int *arr, int *p, int sz)//sz是传入p数组的元素个数
{
    for(int a = 0;a <= sz - 1;a++)
    {
        if(p[a] < 0)
        {
            printf("happy independence number is ,the number of dependent number is:%d   %d\n",arr[a], -(p[a] + 1));//由于前面将1算为依附性幸福数的
        }
    }

    //计算出其是否为质数，且计算其独立性。
}
#include "commonuse.h"

int main()
{
    int * p = NULL;
    int get1, get2;
    scanf("%d %d",&get1, &get2);//默认输入的是闭区间，get2 - get1 +1是数组元素个数
    p = (int *)malloc(sizeof(int)* (get2 - get1 + 1));//决定区间，那么这个时候p就像数组名。一样了，注意这里的*是乘法，不是解引用符号
    int arr[get2 - get1 + 1];//用这个数组来储存和标记数字，对p里面本身存的数来对比
    initial(p, get1 ,get2 );//对p初始化，把输入的数放入数组，方便取用，注意使用了malloc函数不要进行指针位移就ok。
    initial(arr, get1 ,get2 );
    judge(p,get1,get2);
    printresult(arr,p,get2 - get1 + 1);
    free(p);
    p = NULL;
    system("pause");
    return 0;
}

#include "commonuse.h"

// int mystrlen(char const * arr)
// {
//     int a = 0;
//     assert(arr != NULL);
//     while(arr[a])
//     {
//         a++; 
//     }
//     return a;
// }

// int  main()
// {
//     char arr[] = "abcde";
//     printf("%d\n", mystrlen(arr));
//     system("pause");
//     return 0;
// }

//strlen函数，返回类型是unsigned long long
//strcat 函数

//1.函数的被接受函数必须有足够的空间接纳源字符串。
//2.源字符串必须要以\0结尾，否则容易出bug
//3.返回值是被接受字符串的首地址 
//4.追加的字符串会在被接受字符串里面的\0去追加

// char * my_strcat(char * arr1, char const* arr2)
// {
//     char* ret  = arr1;//将被接受字符串首地址存储起来
//     assert(arr1 && arr2);//判断二者不是空指针。
//     while(*(arr1) != '\0')
//     {
//         arr1++;
//     }
//     while(*(arr1 )++ = *(arr2)++)
//     {
//         ;
//     }
//     return ret;

// }
// int main()
// {
//     char arr1 [30]= "hello";
//     char arr2[10] = "world";
//     my_strcat(arr1,arr2);
//     system("pause");
//     return 0;
// }
//上述通过对strcat函数的认为实现，有助于了解。

//strcmp函数，比较字符串，从第一个开始，直到有一个字符不相等,这个函数也是有缺陷的，就是如果一个字符串过于长，
//会导致另外一个字符串越界访问

// int main()
// {
//     char * a = "abcd";
//     char * b = "djiw";
//     strcmp(a,b);//我们发现这个函数值饭返回之整形。
//     strcat(a,b);
//     strlen(a);//而strlen和
//     system("pause");
//     return 0;
// }

//strncmp//注意这个函数比较0个字符串时，默认是相等的字符串
//strncat
//strncpy
//以上三个函数，使用和其原型差不多
//区别是，函数多了一个变量，表示操作的字符个数
//所以strcat和strncpy一样返回被赋值字符串地址·


// char* my_strncpy(char* arr,const char *ar1, unsigned long num)
// {
//     int c = 1;
//     char *ret = arr;
//     assert(arr && ar1);
//     while( num >= c++)
//     {
//         *arr++ = *ar1++;
//     }
//     return ret;
// }
// //assert不要少，const也是
// int main()
// {
//     char arr[] = "abcf";
//     char ar1[] = "mciw";
//     printf("%s\n",strncpy(arr, ar1,2));
//     my_strncpy(arr, ar1, 4);
//     system("pause");
//     return 0;
// }



//strstr字符串查找函数，
//这个函数在查找时，比较字符串，比较到目标字符串\0以前便不在比较，
//然后返回找到字符串的首地址

char * my_strstr(const char* arr1, const char*arr2)
{
    
    int num = 0;
    char * tem = (char*)arr1;//由于，给arr1和arr2定义的事const变量，所以这里需要强制类型转换，这里就是对变量的理解，const类型的变量依旧是变量
    char * tem2 = (char*)arr2;//但是如此操作之后，就需要注意不要用设定的指针改变字符串内容
    assert(arr1&&arr2);
    while(*arr1)
    {
        tem = (char*)arr1;//用临时变量去储存地址的值
        tem2 = (char*)arr2;
        while(*tem && *tem2)//这样在是\0就停止比较。任意一个是\0，就会停止比较。
        {
            if(*tem == *tem2)
            {
                tem++;
                tem2++;
            }
            else{
                arr1++;
                break;
            }
        }
        if(*tem2 == '\0')//如果打印出str2是\0那么就说明比较出字符串。
        {
            return (char*)arr1;
        }
    }
    return NULL;
}

int main()
{
    char *p1 = "abbcd";
    char *p2 = "bc";
    char* p3 = my_strstr(p1, p2);    
    if(p3)//例如这里的p3就是返回的b的地址，
    {
        printf("%s\n", p3);
    }
    else{
        
    }
    printf("%d\n", strcmp(p1,p2));

    system("pause");
    return 0;
}

#include "commonuse.h"
//strcpy函数会追加字符\0。
// int mystrlen(char const * arr)
// {
//     int a = 0;
//     assert(arr != NULL);
//     while(arr[a])
//     {
//         a++; 
//     }
//     return a;
// }

// int  main()
// {
//     char arr[] = "abcde";
//     printf("%d\n", mystrlen(arr));
//     system("pause");
//     return 0;
// }

//strlen函数，返回类型是unsigned long long
//strcat 函数

//1.函数的被接受函数必须有足够的空间接纳源字符串。
//2.源字符串必须要以\0结尾，否则容易出bug
//3.返回值是被接受字符串的首地址 
//4.追加的字符串会在被接受字符串里面的\0去追加

// char * my_strcat(char * arr1, char const* arr2)
// {
//     char* ret  = arr1;//将被接受字符串首地址存储起来
//     assert(arr1 && arr2);//判断二者不是空指针。
//     while(*(arr1) != '\0')
//     {
//         arr1++;
//     }
//     while(*(arr1 )++ = *(arr2)++)
//     {
//         ;
//     }
//     return ret;

// }
// int main()
// {
//     char arr1 [30]= "hello";
//     char arr2[10] = "world";
//     my_strcat(arr1,arr2);
//     system("pause");
//     return 0;
// }
//上述通过对strcat函数的认为实现，有助于了解。

//strcmp函数，比较字符串，从第一个开始，直到有一个字符不相等,这个函数也是有缺陷的，就是如果一个字符串过于长，
//会导致另外一个字符串越界访问

// int main()
// {
//     char * a = "abcd";
//     char * b = "djiw";
//     strcmp(a,b);//我们发现这个函数值饭返回之整形。
//     strcat(a,b);
//     strlen(a);//而strlen和
//     system("pause");
//     return 0;
// }

//strncmp//注意这个函数比较0个字符串时，默认是相等的字符串
//strncat
//strncpy
//以上三个函数，使用和其原型差不多
//区别是，函数多了一个变量，表示操作的字符个数
//所以strcat和strncpy一样返回被赋值字符串地址·


// char* my_strncpy(char* arr,const char *ar1, unsigned long num)
// {
//     int c = 1;
//     char *ret = arr;
//     assert(arr && ar1);
//     while( num >= c++)
//     {
//         *arr++ = *ar1++;
//     }
//     return ret;
// }
// //assert不要少，const也是
// int main()
// {
//     char arr[] = "abcf";
//     char ar1[] = "mciw";
//     printf("%s\n",strncpy(arr, ar1,2));
//     my_strncpy(arr, ar1, 4);
//     system("pause");
//     return 0;
// }



//strstr字符串查找函数，
//这个函数在查找时，比较字符串，比较到目标字符串\0以前便不在比较，
//然后返回找到字符串的首地址

char * my_strstr(const char* arr1, const char*arr2)
{
    
    int num = 0;
    char * tem = (char*)arr1;//由于，给arr1和arr2定义的事const变量，所以这里需要强制类型转换
    char * tem2 = (char*)arr2;//但是如此操作之后，就需要注意不要用设定的指针改变字符串内容
    assert(arr1&&arr2);
    while(*arr1)
    {
        tem = (char*)arr1;//用临时变量去储存地址的值
        tem2 = (char*)arr2;
        while(*tem && *tem2)//这样在是\0就停止比较。任意一个是\0，就会停止比较。
        {
            if(*tem == *tem2)
            {
                tem++;
                tem2++;
            }
            else{
                arr1++;
                break;
            }
        }
        if(*tem2 == '\0')//如果打印出str2是\0那么就说明比较出字符串。
        {
            return (char*)arr1;
        }
    }
    return NULL;
}

int main()
{
    char *p1 = "abbcd";
    char *p2 = "bc";
    char* p3 = my_strstr(p1, p2);    
    if(p3)//例如这里的p3就是返回的b的地址，
    {
        printf("%s\n", p3);
    }
    else{
        
    }
    printf("%d\n", strcmp(p1,p2));

    system("pause");
    return 0;
}

#include "commonuse.h"
// int main()
// {
//     char a[] = "abcd";
//     char p[1];
//     strcpy(p,a);
//     printf("%s\n",p);
//     system("pause");
//     return 0;
// }

//strtok函数
int main()
{
    char a[5] = {'h','.','l','.','w'};
    char b[92]  = "eeeee0000\0eeeee";
    char* c = ".";
    strcpy(b, a);
    b[5] = 'e';
    char* ret  = strtok(b, c);
    for(;ret != NULL;)
    {
        printf("%s  \n", ret);
        ret = strtok(NULL,c);
        if(ret == NULL)
        {
            ret = &(b[9]);
        }
    }
    system("pause");
    return 0;
}

//上述使用中，我们发现，这个函数的使用，就是对给定的源字符串，
//在被动字符串中，逐一找出字符，并且将该字符变为\0，并且返回首字符地址，
//并且记住变为\0字符的下一个字符的地址，下一次再调用时，只需要将被动字符串改为空指针即可
//当遇见\0的时候，就会会停止，并且返回本次调用的首元素地址，但是函数就不再会再记住下一个地址，并且下一次再以空指针调用这个函数时
//这个函数就会直接返回空指针。




#include "commonuse.h"
// int main()
// {
//     char a[] = "abcd";
//     char p[1];
//     strcpy(p,a);
//     printf("%s\n",p);
//     system("pause");
//     return 0;
// }

// //strtok函数
// int main()
// {
//     char a[5] = {'h','.','l','.','w'};
//     char b[92]  = "eeeee0000\0eeeee";
//     char* c = ".";
//     strcpy(b, a);
//     b[5] = 'e';
//     char* ret  = strtok(b, c);
//     for(;ret != NULL;)
//     {
//         printf("%s  \n", ret);
//         ret = strtok(NULL,c);
//         if(ret == NULL)
//         {
//             ret = &(b[9]);
//         }
//     }
//     system("pause");
//     return 0;
// }

//上述使用中，我们发现，这个函数的使用，就是对给定的源字符串，
//在被动字符串中，逐一找出字符，并且将该字符变为\0，并且返回首字符地址，
//并且记住变为\0字符的下一个字符的地址，下一次再调用时，只需要将被动字符串改为空指针即可
//当遇见\0的时候，就会会停止，并且返回本次调用的首元素地址，但是函数就不再会再记住下一个地址，并且下一次再以空指针调用这个函数时




//strerror函数，输入值是整形。返回一个字符串。
//errno是一个全局变量，监视库函数的执行情况，有对应的错误就会反回相对应的值。
//而再把值拿给strerror函数就会返回出是什么错误


// int main()
// {
//     FILE* pf = fopen("commonuse.h","r");
//     printf("%s\n",strerror(errno));//我们就会发现是无错误，返回不同值，对应不同错误。
//     system("pause");
//     return 0;
// }


//字符判断函数
//iscntrl:判断是否为控制字符,是就返回非0的数，不是就返回0；常见控制字符，换行,水平制表，del等
//isspace：kongbaizifu：空格，换页，换行，回车，水平制表，垂直制表
//isdigit：十进制数字0-9
//isxdigit：十六进制数字包含十进制数字和小大写字母a-fA-F.\xhh表示16紧致数
//islower：是否为小写字母
//isupper：是否为大写字母
//isalpha：是否是字母
//isalnum：是否是字母或者数字a-z,A-Z,0-9
//ispunct：是否为标点
//isgraph：是否为图形字符
//isprint：打印任何字符

// int main()
// {
//     char a = '\t';
//     printf("%d",iscntrl(a));
//     char b[] = '我';
//     printf("%d", isxdigit(b));
//     system("pause");
//     return 0;
// }


//字符转换：tolower//替换为小写字符
//          toupper//i替换为大写字符



#include "commonuse.h"
//内存操作函数

//mencpy函数，对指定字节进行拷贝到对应数组
//这个函数则对任意类型都可以进行拷贝，是直接对内存进行操作。
//即使是结构体或，结构体数组，二维数组（二维数组相当于存了n行一维数组），者指针数组，数组指针（整个数组的地址）也可以。
// int main()
// {
//     int arr[] = {1,2,3,4,5};
//     int arr2[6];
//     memcpy(arr2,arr,sizeof(arr));//这个函数搭配sizeof使用很方便
//     system("pause");
//     return 0;
// }

// int my_bottle(int a)
// {
//     int b,d;//c做瓶数，b做余下的瓶数
//     for(d = 20;a > 1;)
//     {
//         b += a%2;//把可能余的1保留在b
//         d += a/2;//由于c语言整形是直接甩掉尾数，所以这里不用考虑1的问题
//         a/=2;//算出下一次瓶数
//         a+=b;
//         b = 0;
//     }
//     return d;
// }

// int main()
// {
//     int bottle = 20;
//     printf("%d\n", my_bottle(bottle));
//     system("pause");
//     return 0;
// }
// void * my_memmove(void* dest,void * sor,size_t count)
// {
//     assert(dest&&sor);
//     void *a = dest;
//     if(dest > sor)
//     {
//         while(count--)
//         {
//             *((char*)dest + count) = *((char*)sor + count);
//         }
//     }
    
//     else if(dest < sor)
//     {
//         char* c = (char*)dest;
//         char* d = (char*)sor;
//     while(count--)
//     {
        
//         *((char*)c) = *((char*)d);
//         c++;d++;
//     }
//     }
//     return a;
// }


// int main()
// {
//     int arr[5] = {1, 2, 3, 4, 5};
//     my_memmove(arr, arr+2,12);
//     system("pause");
//     return 0;
// }

//memcmp
// int main()
// {
//     int a[] = {1,2,3,4,5};
//     int b[] = {1,2,4,3,5};
//     printf("%d\n", memcmp(a,b,9));//结果-1
//     system("pause");
//     return 0;
// }
//与字符串比较函数类似，但是是一个一个字节比较
//那么就涉及小端储存以及大端储存问题，如下
// int main()
// {
//     int a[] = {1,2,17,4,5};
//     int b[] = {1,2,4,3,5};
//     printf("%d\n", memcmp(a,b,9));//结果1
//     system("pause");
//     return 0;
// }

//这里就是为什么说，小段储存，因为低位存在低地址，所以，17，是01 01 00 00导致大小比较结果不同

// int main()
// {
//     short a[] = {1,2,3,4,5};
//     memset(a,-1,20);//这里值得注意的是memset函数改变，依旧是字节字节得改，所以这里输入50，那么就把5整形截断，改变后放入进去
//     system("pause");
//     return 0;
// }


#include "commonuse.h"

struct S {
    int c;
    char b;
    double d;
    char arr[10];
}a;
struct S1 {
    struct S f;
    int m;
};

// int main()
// {
//     printf("%d\n", sizeof(a));//打印结果发现空间是32
//     printf("%p\n", &(a.c));//980
//     printf("%p\n", &(a.b));//984
//     printf("%p\n", &(a.d));//988
//     printf("%p\n", &(a.arr));//990.数组的对齐取决于内存数组的数据类型
//     system("pause");
//     return 0;
// }
// 出现上述结果与内存存储有关。首先，一般认为，为了提升内存运行速度
//n字节大小的变量，就会存在其地址是n字节的整数倍的地址上
//这也是为什么，c的地址是980而不是981.




//结构体变量的解释。一般结构体里面变量会有一个对齐数（简称为am（Alignment number））
//这个am取决于编译器的默认对齐数和变量字节数二者的较小值。
//同时结构体还有一个0地址为，也就是开始储存的那个地址。

//结构体里面变量的地址：1.如果是第一个变量的地址，则按照常规储存，即满足其字节数的整数倍
//                     2.其他变量在存储的时候的，取与0地址的偏移量为对齐数整数倍的地址开始储存，此时不会按照常规的储存使地址使类型字节数的整数倍
//                     3.结构体的总大小为最大对齐数的整数倍，每一个变量有对应的对齐数（注意这里是与默认对齐数计算之后得到的对齐数），在这些对齐数之中最大值
//                     4.如果存在其嵌套结构体，那么被嵌套的那个（被包含）结构体,例如上述的struct S就是，那么其作为成员的对齐数，是其内部的最大对齐数
//                     5.注意结构体没有前面变量所谓的地址整除字节。但是其有对齐数整除现象，也就是其地址必须能整除其的最大对齐数。比如把对齐值改为7（随然报错，但是可以试一下）
//                      6.同类型数组会相互分配空间，就比如char[20]就可以不去对齐，接在上一个char数组后面


//offsetof，用来计算结构体里面得变量得偏移量de宏,头文件是stddef
//%d = offsetof(结构体变量类型（不是结构体变量如a），结构体里面得变量)

// struct S {
//     int c;
//     char b;
//     double d;
//     char arr[40];
// }a;
// struct S1 {
//     struct S f;
//     int m;
// };

// int main()
// {
//     printf("%d\n", offsetof(struct S ,c));
//     printf("%d\n", offsetof(struct S ,b));//偏移量就是4
//     printf("%d\n", offsetof(struct S,arr));
//     system("pause");
//     return 0;
// }


//结构体的函数传参，一般传地址，一则，传结构体大，二则，传递至才能改变值。


// #include "commonuse.h"
// //位段，
// //1.位段可以通过结构体实现，
// //2.其成员必须是整形（也就包含char），且往往统一
// //3.位段成员名后面有一个冒号和一个数字
// //5.位段开辟空间的方式是以4个字节或者1个字节来开辟。
// //6.按照开辟放下的成员,例如int，4个字节4个字节的拿
// //位段一般不考虑跨平台问题，因为
// //1.int被当成有符号数还是无符号数是不确定的
// //2.位段最大位的护目不能确定，（16为机器是16，32位机器是32）
// //位段成员从右还是从左分配时不确定的
// //当一个结构包含两个位段时，第二个位段成员比较大，无法容纳第一个位段剩余的位的时候
// //时舍弃剩余的位，或者是利用，是不去欸的那个的
// struct S
// {
//     int a :1;
//     int b :5;
//     int c :10;//第一个4个字节这里存abc，剩下两个空间浪费掉
//     int d :30;//第二个四个字节，存d，
// };//一个元素必须放在一整块空间里面。这也就代表不能大于整形的字节
// //总体来说，位段就是为了节省空间的。
// int main()
// {
//     printf("%d\n",sizeof(struct S));
//     system("pause");
//     return 0;
// }

