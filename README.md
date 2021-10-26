#define _CRT_SECURE_NO_WARNINGS 1

#include<stdio.h>

#include<Windows.h>

int main()

{

	int Message_Num = 100;
  
	char  name;
  
	printf("输入你要轰炸的对象：\n");
  
	scanf("%s",&name);
  
	printf("输入你要轰炸的次数：\n");
  
	scanf("%d", &Message_Num);
  
	HWND H = FindWindow(0,"name");
  
	while (Message_Num>0)
  
	{
  
		SendMessage(H, WM_PASTE, 0, 0);
    
		SendMessage(H, WM_KEYDOWN, VK_RETURN, NULL);
    
		Message_Num--;
    
	}
  
	return 0;
  
}

