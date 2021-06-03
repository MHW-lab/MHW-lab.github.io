---
layout: single
title: "수행 평가 정리"
toc: true
toc_sticky: true
toc_label: "페이지 주요 목차"
categories: "형성평가"
---


### 01. 사주보기
연도, 월, 일을 입력하여 출생 연도 -월 +일의 계산 결과를 토대로 사주를 본다. 마지막 숫자가 0이면 대박, 0이 아니면 그럭저럭을 출력한다. 
~~~c
#include <stdio.h>
 int main(void)
{int year, month, day, result;

printf("당신의 사주를 봐드립니다."\n);
printf("연도 월 일을 차례대로 입력하세요: ");
scanf("%d %d %d", &year, &month, &day);

result=(year-month+day)%10;
if(result==0)
printf("당신의 사주는 대박입니다.\n");
else
printf("당신의 사주는 그럭저럭입니다.\n");
return 0;
}
~~~
---

### 02. 3개의 터널 통과
터널 높이를 각각 입력하고, 170cm인 자동차가 이를 무사 통과하면 "무사 통과"를 출력하고, 충돌이 일어나면 충돌 터널 높이를 출력한다.
~~~c
#include <stdio.h>
int main(void)
{ int tunnul_1, tunnul_2, tunnul_3;
printf("세 터널의 높이를 차례대로 입력하세요 : ");
scanf("%d,%d,%d",&tunnul_1,&tunnul_2,&tunnul_3);

if(tunnul_1<=170)
printf("충돌 %d", tunnul_1);
else if(tunnul_2<=170)
printf("충돌 %d", tunnul_2);
else if(tunnul_3<=170)
printf("충돌 %d", tunnul_3);
else
printf("무사 통과");
return 0;
}
~~~ 
---

### 03. 이달은 며칠까지 있을까 
연도와 월을 알고 있을 때 그 달의 마지막 날을 구하는 프로그램을 작성하라. 윤년 또한 포함한다. 
~~~c
#include <stdio.h>
int main(void)
{int year, month;
printf("연도와 월을 입력하세요 : ");
scanf("%d%d", &year, &month);
printf("%d년 %d월의 마지막날은 ", year, month);

if(month==1||month==3||month==5||month==7||month==8||month==10||month==12)
printf("31일");
else if(month==4||month==6||month==9||month==11)
printf("30일");
else
{
if((year%4==0 && year%100!=0) || year%400==0
printf("29일");
else
printf("28일");
}
printf("입니다.\n");
return 0;
}
~~~
---

### 04. 30분 전
시간과 분이 주어지면 30분 전의 시간을 계산해주는 프로그램램을 작성하시오.
~~~c
#include <stdio.h>
 
int main(void) {
 
int hour, minute;
printf("시간과 분을 순서대로 입력하세요: ");
scanf("%d %d", &hour, &minute);
 
if(minute>=30)
printf("입력 시간의 30분 전의 시간은 %d시 %d분입니다.", hour, minute-30);
 
else
if(hour==0)
printf("입력 시간의 30분 전의 시간은 12시 %d분입니다", minute+30);
else
printf("입력 시간의 30분 전의 시간은 %d시 %d분입니다", hour-1, minute+30);
 
return 0;
}
~~~
---

### 05. 도어락
주인이 장치를 선택하여 등록된 값을 입력하고 문을 개폐하는 프로그램을 작성하라. IC카드 값은 'c' 비밀번호는 24680 지문 등록 값은 1.2345678이며, 정상 인증되면 "문 열림"을 출력하고 아니면 "디리릭디리릭!"을 출력한다. 
~~~c
#include <stdio.h>
 
int main(void) {
int enter;
float password;
double fingerprint;
char ICcard;
 
printf("장치 선택: ");
scanf("%d", &enter);
 
if (enter==1){
 printf("IC카드: ");
 scanf(" %c", &ICcard);
 {if(ICcard=='c')
 printf("문 열림~~");
 else
 printf("디리릭!디리릭!");
 }}
 
else if(enter==2){
 printf("비밀번호: ");
 scanf(" %f", &password);
 {if(password==24680)
 printf("문 열림~~");
 else
 printf("디리릭!디리릭!");
 }}
 
else
{printf("지문: ");
 scanf("%.7f", &fingerprint);
 {if(fingerprint==1.2345678)
 printf("문 열림~~");
 else
 printf("디리릭!디리릭!");
 }}
 
 return 0;
}
~~~
---

### 06. 가위바위보
컴퓨터가 임의의 값을 가지고 있을 때, 사용자가 가위, 바위, 보 중 하나를 입력하여 그 결과를 출력하는 프로그램을 작성하시오. 
~~~c
#include <stdio.h>
 
int main(void) {
 char user, com;
 com='r';
 
 printf("r/s/p: ");
 scanf(" %c", &user);
 
 if(user==com) printf("비겼다");
 else if ((com=='r'&&user=='s')|| (com=='s' && user=='p')|| (com=='p' &&user=='r'))
 printf("졌다");
 else printf("이겼다");
 
 return 0;
}
~~~
---
