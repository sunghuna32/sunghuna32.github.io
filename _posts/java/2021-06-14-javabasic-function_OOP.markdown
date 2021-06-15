---
layout: post 
title:  "5-7강 : 조건문, 반복문, 예외처리"
subtitle:   ""
categories: java
tags: javabasic
order: 2
comments : true
---
> 자바기본_5-7강<br>
> 조건문, 반복문, 예외처리

### 5강 : 조건문
1. 조건문이란…?
    - 참 거짓 을 통해 코드를 선택적으로 실행이 가능한 조건문입니다
    ~~~ java 
    if(){
    } else if(){
    } else{
    }
    ~~~
    - (조건식)?True일 때 Return : False일 때 Return    
      : score<10?”10점 이하”:”10점 이상”
    -  SWITCH(변수) { CASE 조건1 : 실행1 break; CASE조건2 : 실행2 break; }
    ~~~ java
     : SWITCH(score) {
        case 100:
            sout(“만점입니다.”);
            break;
        case 99:
            sout(“99점입니다.”);
            break;
         …
        default :
            sout(“111”)
            break;
     }
    ~~~

###  6강 : 반복문
1. 반복문이란…?
    - 반복해서 어떤 작업을 하고자 할 때 간단하게 표현할 수 있게해준다.

2. while
    - while(boolean){}

3. do-while
    - 무조건 한번은 실행함. 2번째 실행부터 while문처럼 조건을 체크한다.
    - do{}while(boolean)

4. for
    - 몇번 반복할지 정확히 알고있는 경우 while대신 for문을 권장합니다.
    - for(int i=0; i<10;i++){}

5. for-each
    - collection에 저장된 모든 값을 사용하여 반복
    - for(String s : ary){}


   
###  7강 :예외처리
 - 예외처리란…? 오류가 발생할 만한 데에 사용하여 오류를 쉽게 찾고 수정할 수있게 끔 한다. 프로그램이 멈추지 않게 한다.
 - try, catch, finally를 사용
 - try{실행코드} catch (exception종류 변수){오류처리코드} finally{}
 - throw를 통해 오류를 던질 수 있다.
 - finally는 오류 발생 여부와 상관 없이 작동함
 - exception을 상속받은 class 를 통해서 특정 오류만 잡아내는 것도 가능
 - catch 로 명시적으로 하지 않고 Throw Exception을 통해서 콜한 함수에서 수행하게 할 수도 있다.

 