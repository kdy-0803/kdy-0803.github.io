---
layout: single
title: ""
toc: true
toc_sticky: true
toc_label: "페이지 주요 목차"
---


### 01. 보안 카드 접수증
~~~c
#include <stdio.h>
int main()
{
   char name[11];
   int age;
   char code[2];
   float secure;
 
   printf("이름을 입력하세요 : ");
   scanf("%s", name);
 
   printf("나이를 입력하세요 : ");
   scanf("%d", &age);
 
   printf("부서코드를 입력하세요 : ");
   scanf("%s", code);
 
   printf("보안키를 입력하세요 : ");
   scanf("%f", &secure);
 
   printf("**************************\n");
   printf("이름 : %s\n", name);
   printf("나이 : %d\n", age);
   printf("부서코드 : %s\n", code);
   printf("보안키 : %.3f\n", secure);
   printf("**************************\n");
}

~~~

### 02. 성적계산

~~~c
#include <stdio.h>
 
int main()
{
   float a, b, c;
   int d, e, f;
   float score;
   printf("***과목별 점수 계산 프로그램 ***\n");
   printf("중간고사 반영비율/받은 점수를 입력하세요 : ");
 
   scanf("%f %d", &a, &d);
   printf("기말고사 반영비율/받은 점수를 입력하세요 : ");
   scanf("%f %d", &b, &e);
   printf("수행평가 반영비율/받은 점수를 입력하세요 : ");
   scanf("%f %d", &c, &f);
 
   score = (a*d) + (b*e) + (c*f);
   printf("점수는 %.1f입니다.\n", score);
}
~~~

### 03. 사주보기

~~~c
int main(){
 int yr, m, d, luck;
 
 printf("당신의 사주를 봐드립니다.\n연도 월 일을 차례대로 입력하세요 : ");
 scanf("%d %d %d", &yr, &m, &d);
 luck=(yr-m+d)%10;
 
 if (luck==0)
   printf("당신의 사주는 대박입니다.\n");
 else
   printf("당신의 사주는 그럭저럭입니다.\n");
 
 return 0;
}
~~~

### 04. 3개의 터널 통과

~~~c
int main(void) {
 int a, b, c;
 printf("세 터널의 높이를 차례대로 입력하세요 : ");
 scanf("%d %d %d", &a, &b, &c);
 if (a<=170)
     printf("충돌 %d", a);
 else if (b<=170)
     printf("충돌 %d", b);
 else if (c<=170)
     printf("충돌 %d", c);
 else
   printf("무사 통과");
 
return 0;
}
~~~

### 05. 이 달은 며칠까지 있을까?

~~~c
int main(void) {
 int year, month;
 printf("연도와 월을 입력하세요 : ");
 scanf("%d%d", &year, &month);
 printf("%d년 %d월의 마지막날은, ", year, month);
 
 if (month==1||month==3||month==5||month==8||month==10||month==12)
   printf("%d", 30);
 else if (month==4||month==6||month==9||month==11)
   printf("%d", 30);
 else{
   if ((year%4==0)&&!(year%100==0))||(year%400==0))
     printf("29");
   else
     printf("28");
 }
 printf("입니다\n");
}
~~~

### 06. 30분 전

~~~c
int main() {
 int h, min;
 printf("시간과 분을 입력하세요 : ");
 scanf("%d %d", &h, &min);
 printf("입력한 시간의 30분 전 시간은 ");
  if (min>=30)
   printf("%d시 %d분", h, (min-30));
 else{
   if(h==0)
     printf("%d시 %d분", 23, (30+min));
   else
     printf("%d시 %d분", h-1, (30+min));
 }
 
 return 0;
}
~~~


### 07. 도어락

~~~c
#include <stdio.h>
 
int main(void) {
 int select;
 char dic='c', ic;
 int dpw=24680, pw;
 double dfig=1.2345678, fig;
 
 printf("장치 선택: ");
 scanf("%d", &select);
 
 if(select==1){
   printf("IC 카드:");
   scanf(" %c", &ic);
 }else if(select==2){
   printf("비밀번호: ");
   scanf("%d", &pw);
 }else{
   printf("지문: ");
   scanf("%d", &pw);
 }
 if(dic==ic || dpw==pw || dfig==fig)
   printf("문 열림~");
 else
   printf("디리릭!디리릭!");
 
 return 0;
}
~~~

### 08. 가위바위보

~~~c
#include<stdio.h>
int main(){
 char a, b;
 a='s';
 
 printf("입력(가위:s, 바위:r, 보:p): ");
 scanf("%c", &b);
 
    if (b=='s') printf("비겼다.");
   else if (b=='r') printf("이겼다.");
   else printf("졌다.");
 
 return 0;
}
~~~

