---
layout: post 
title:  "8-9강 : 함수, 객체지향프로그래밍"
subtitle:   ""
categories: java
tags: javabasic
order: 2
comments : true
---
> 자바기본_8-9강<br>
> 8강 : 함수
> 9강 : 객체지향프로그래밍

### 8강 : 함수
1. 함수란…?
    -  특정한 목적, 기능을 하도록 정의된 코드가 모인것
    - 재사용가능이 높은 것을 함수로 만든다 => 코드의 재사용

2. 메소드(method)와 함수(function)의 엄밀한 차이
   - 함수는 독립된 코드. 메소드는 class내에 선언된 함수
   - 그러나, 구분 없이 막 쓰인다.

3. 사용    
   - varType methodName (varType varName, varType varName2) {  
     return returnVar  
   }
4. Static
   - class 에서 바로 호출 가능
   - static함수에서 static이 아닌 것을 호출 하면 오류가 난다.
   - static이 아닌 것은 객체를 만들어서 호출을 해주어야 한다.

   
###  9강 : 객체지향프로그래밍
1. 객체지향프로그래밍이란…?  
   - 현실 세계의 모든 것을 사물을 객체=Class로서 바라보는 것
2. Member 변수
   - class 내부에 선언된 변수?
3. 생성자 (Constructor)
   - 멤버의 초기화 등을 사용할때 사용
~~~java   
   public class ClassName (){  
      member1 ,member2;  
      public ClassName(varType varName){     
      member1 = varName
      }
   }
~~~
4.  접근 제어자 요약
- private: private로 선언된 함수,맴버변수,생성자는 선언된 클래스내부에서만 접근 가능.
- public: public으로 선언된 클래스,함수,맴버 변수,생성자는 모든 다른 클래스에서 접근 가능.
- default: private,public등 접근 제어자 미사용시 클래스,함수,맴버변수,생성자는 동일한 패키지에서만 접근 가능.
- protected: 함수,맴버변수,생성자는 동일패키지 또는 다른 패키지의 하위 클래스에서만 접근 가능.    
   =>접근권한 범위:public>protected>default>private
- final: 클래스에 사용시 다른 클래스에서 상속 불가능.
  메소드,멤버 변수에 사용시 오버라이딩,수정 불가.
- static: 메소드,멤버 변수에 사용. 클래스에 속하게되며 객체의 생성없이 바로 접근가능.
- abstract: 클래스에 사용시 객체생성 불가능. 오직 다른클래스가 상속받아서 사용해야함.
  메소드에 사용시 오직 abstract 클래스에서만 abstract 메소드 정의가능. 메소드
  바디(중괄호)부분이 없음.     
  (메소드의 예: abstract void run(); 바디부분은 상속받은 곳에서 기능에 맞게 작성.)
