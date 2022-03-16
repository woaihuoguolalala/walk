# walk
no
#include<Windows.h>
#include<conio.h>
#include<stdio.h>
#include<string.h>
char a[11][15]={
"*#*********",
"***###*###*",
"###**#****#",
"*#**###**#*",
"***********",
"#####*##*##",
"**#*****#*E",
"***#*###**#",
"*#*********", 
};
int Q=14,Z=11,R,i
int x,y;
void print_person()
{
	COORD pos;
	pos.X=x;
	pos.Y=y;
	printf("curX=%d,curY=%d",x,y);
	SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE),pos);
}
void print_map()
{
	for(i=0;i<B;i++)
	{
		puts(a[i]);
	}
 } 
 void print_move(char Z)
 {
 	switch(b)
 	{
 		case 'W':y--;
 		if(y<0)
 		y=0;
 		if(a[y][x]=='#')
 		y++;
 		break;
 		case 'S':y++;
 		if(y>=Z)
 		y=Z-1;
 		if(a[y][x]=='#')
 		y--;
 		break;
 		case 'A':x--;
 		if(x<0)
 		x=0;
 		if(a[y][x]=='#')
 		x++;
 		break;
 		case 'D':x++;
 		if(x>=Q)
 		x=Q-1;
 		if(a[y][x]=='#')
 		x--;
 		break;
	 }
 }
 int main()
 {
 	char t;
 	while(1)
 	{
 		system("cls");
 		print_map();
 		print_person();
 		t=getch();
 		print_move(t);
 		if(a[y][x]=='E')
 		{
 			printf("恭喜通关！\n");
 			break;
		 }
	 }
	 return 0;
 }
