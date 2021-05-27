---
layout: single
title: "조건문"
toc: true
toc_sticky: true
toc_label: "페이지 주요 목차"
categories: "형성평가"
---

### 01. 사주보기
![saju](/assets/images/IT활돌_사주보기.png)
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
