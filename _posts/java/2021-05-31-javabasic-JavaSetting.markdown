---
layout: post 
title:  "Posting templates"
subtitle:   ""
categories: java
tags: javabasic
order: 2
comments : true
---
> 자바기본_1강<br>
> 자바언어 설명, 설치

###1. JVM , JRE, JDK 설명
 - 자바소스코드 -> 컴파일 -> .class 바이트 코드 생성        
 - JVM: 바이트코드(.class)를 읽고,검증,실행, 동일한 실행환경을 보장 받는다.
 - JRE: JVM에 자바라이브러리,기타 파일들을 가지고 있음. 자바를 실행하기위한 프로그램.
 - JDK:JRE,컴파일러등 개발도구를 포함하는 프로그램    
   ![jdktojvm]../assets/img/jdktojvm.png


### 'tab'을 활용하여 들여쓰기 가능

### 탭을 활용하여 들여쓰기 Test
    1. 문단
        1)들여쓰기 문단1
            a. 들여들여쓰기 문단1
                -
                -
            b. 들여들여쓰기 문단2
        2)들여쓰기 문단2

### ~~~ 를 황용하여 코드를 쓰자
~~~ java
public class RecommendID {
    public static void main(String[] args)  {
        System.out.print("Enter ID : ");
        Scanner inStr = new Scanner(System.in);
    }
}
~~~

