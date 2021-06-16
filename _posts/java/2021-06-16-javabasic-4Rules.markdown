---
layout: post 
title:  "10-13강 : OOP의 4가지 특성"
subtitle:   ""
categories: java
tags: javabasic
order: 2
comments : true
---
> 자바기본_10-13강<br>
> 10강 : 캡슐화  
> 11강 : 상속  
> 12강 : 다형성     
> 13강 : 추상화 


### 10강 : 캡슐화 (Encapsulation)
1. 캡슐화란…?
    - 필요한 속성(Attribute) 와 행위(Method) 를 하나로 묶고,  
      그 중 일부를 외부에서 사용하지 못하도록 은닉하는 것

2. 캡슐화의 주된 목적 :  "데이터의 은닉"
    - 민감한 데이터를 private로 감춘다.
    - public의 setter 또는 getter 메소드로만 private로 감춘 데이터에 접근 혹은 수정하게 한다.    
        => private변수에 선택접 접근(read-only 또는 write-only)을 제어할 수 있게 된다.
    - public보다 보안성이 증가되며 멤버변수와 함수를 더 좋게 제어 할 수 있게된다.

3. 데이터 은닉의 또다른 목적
    - 유연성:같은 타입을 다루는 자료형에서 Map,Stack,queue와 같은 Collection변경을 class내부의 일부분만 변경을 통해 자료형을 변경할 수 있다.
    - 초기화 작업을 class에서 모아서 처리함으로써 초기화 도중 데이터의가공이 일어날 경우 일부분만 변경하면 된다.

~~~java
[Car.class]

public class Car {
    //Car Object의 Data는 Private로 선언
    private String type;
    private int position;
    private String maker, name;

    //Constructor
    public Car() {
        type = "자동차";
        position = 0;
    }

    //외부에서 Member 접근 가능하게 한다.
    public String getMaker() {
        return maker;
    }

    public void setMaker(String maker) {
        this.maker = maker;
    }

    //외부에서는 Object의 Postion을 변경하지 못하게 한다.
    //=> forword를 통해서만 접근가능
    public void forward() {
        position++;
    }
}
~~~

~~~java
[OOPTest.class ]
public class OOPTest {
    public static void main(String[] args) {
        Car myCar = new Car();
        System.out.println("Init객체 |Type : " +myCar.getType() +" |Position : "+myCar.getPosition()
                +" |Maker : "+ myCar.getMaker()+ " |Name : "+myCar.getName());

        myCar.setMaker("BMW");
        myCar.setName("붕붕이");
        myCar.forward();

        System.out.println("변화후객체 |Type : " +myCar.getType() +" |Position : "+myCar.getPosition()
                +" |Maker : "+ myCar.getMaker()+ " |Name : "+myCar.getName());

    }
}
~~~

~~~
Init객체 |Type : 자동차 |Position : 0 |Maker : null |Name : null   
변화후객체 |Type : 자동차 |Position : 1 |Maker : BMW |Name : 붕붕이
~~~

### 11강 : 상속 (Inheritance)