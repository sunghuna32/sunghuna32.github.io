---
layout: post 
title:  "Posting templates"
subtitle:   ""
categories: tip
tags: tip
order: 2
comments : true
---
> 마크다운 문법을 활용하여 Posting할때 쓰일 템플릿들을 미리 만들어 놓자 <br>
> 참조 : https://eungbean.github.io/2018/06/11/How-to-use-markdown/


### '#'은 헤더로 사용
'#' 1.타이틀

'##' 2. 타이틀

'###' 3.타이틀

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

### 이미지 넣는 법
`![이미지 이름](이미지 주소)`
![jdktojvm](../assets/img/jdktojvm.png)


### Table 만드는 법 
| First Header  | Second Header | Third Header         |
| :------------ | :-----------: | -------------------: |
| First row     | Data          | Very long data entry |
| Second row    | **Cell**      | *Cell*               |
| Third row     | Cell that spans across two columns  ||

