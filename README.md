# -2
/*#include<stdio.h>
//演示多个字符从两端移动，向中间汇聚
#include<string.h>
#include<windows.h>//windows程序重要头文件
#include<stdlib.h>//标准库头文件
int main()
{
	//Welcome to Hogwarts!!!!!
	char arr1[] = "Welcome to Hogwarts!!!!!";
	char arr2[] = "########################";
	int left=0, right,n;
	n = sizeof(arr1) / sizeof(arr1[0])-2;
	//right = strlen(arr1) - 1;右下标=数组长度-1
	right = n;
	while (left <= right)
	{
      arr2[left] = arr1[left];
	  arr2[right] = arr1[right];
	  printf("%s\n", arr2);
	  Sleep(1000);//单位是毫秒，1000毫秒就是一秒windows
	  system("cls");//执行系统命令的函数 即每输出一次清屏操作
	  left++;
	  right--;
	}
	printf("%s", arr2);
	return 0;
}*/
/*#include<stdio.h>
#include<string.h>
//模拟用户登陆情景，且只能登陆三次(只允许输入三次密码，如果密码正确则提示登陆成功，若三次均错误则退出程序)
int main()
{
	int i = 0;
	for (i = 0; i <3; i++)
	{
		char password[20] = { 0 };
		printf("请输入密码:");
		scanf("%s", password);
		if (strcmp(password,"criminal.police")==0  )//==不能用来判断两个字符串是否相等必须用strcmp函数进行比较
		{
			printf("登陆成功\n");
			break;
		}
		else
		{
			printf("密码错误\n");
		}
	}
	if (i == 3)
	{
		printf("三次密码均错误，退出程序\n");
	}
	return 0;
}*/
#include<stdio.h>
#include<math.h>
//用公式π/4≈1-1/3+1/5-1/7+...求π的近似值直到发现某一项的绝对值小于10的-6次方
int main()
{
	int sign = 1;
	double pai = 0.0, n = 1.0, term = 1.0;
	while (fabs(term) >= 1e-6)
	{
		pai += term;
		n = n + 2;
		sign = -sign;
		term = sign / n;
	}
	pai = pai * 4;
	printf("π=%.8f", pai);
	return 0;
}
