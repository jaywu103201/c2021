```

#include "stdio.h"
#include "stdlib.h"
int main(void)
{
	struct data{
		char name[10];
		int score[3];
		int total = 0;
	};
	
	data student[3];
	
	for(int i=0; i<3; i++){
		printf("請輸入學生姓名:");
		scanf("%s",student[i].name);
		
		printf("請輸入國文成績 :");
		scanf("%d",&student[i].score[0]);
		
		printf("請輸入英文成績 :");
		scanf("%d",&student[i].score[1]);
		
		printf("請輸入數學成績 :");
		scanf("%d",&student[i].score[2]);
		for(int j=0; j<3; j++){
			student[i].total += student[i].score[j]; 
		}
	}
	
	for (int i =0; i <3; i++){
		printf("姓名: %s,   國文:%d,  英文:%d,  數學:%d, 總分:%d",
		student[i].name, 
		student[i].score[0],  
		student[i].score[1],  
		student[i].score[2],
		student[i].total);
		printf("\n");
	}
	return 0;
}

```
