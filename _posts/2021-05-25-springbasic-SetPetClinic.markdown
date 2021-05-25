---
layout: post 
title:  "Set Pet Clnic"
subtitle:   ""
categories: springbasic
tags: springbasic
order: 1
comments : true
---
> Spring을 공부하기 Pet Clinic 프로젝트를 세팅해보자  
>> 프로젝트 설정  
>> 프로젝트 살펴보기   
>> 프로젝트 과제풀이

# Pet Clinic 설정 및 살펴보기

### Pet Clinic 설정
1. 프로젝트 복사  
   - 주소 : https://github.com/spring-projects/spring-petclinic
2. Maven Pakage Build
   - ./mvnw package
      - 메이블 빌드하다가 Error 발생
      - 원인 : JAVA_HOME이 설정 되지 않았다
      - 조치 : JAVA_HOME 재설정
        - https://jmsst.tistory.com/11 참고
        - 인텔리 J 재실행

3. Pet Clinic 실행
   - java -jar target/*jar  
     (pakage의 타입을 지정하지 않았기 때문에 .jar로 build 된다.)
4. 이것저것 눌러보기
5. 어플리케이션 실행방법 
   - .../src/main/java/org/springframework/samples/petclinic/PetClinicApplication.java
6. 어플리케이션 종료방법
    - ctrl+c

### Pet Clinic 살펴보기
1. 작동구조 흐름  
    -> Event 호출  
    -> dispatcherServelet이 GetMapping Annotation을 참고하여 컨트롤러의  initCreationForm를 호출  
    -> model을 만들고 view를 리턴
2. 과제
   first name 으로 검색하게 수정
   key word 를 포함하고 있는 걸로 바꿔 보기
   owner에 나이를 추가해 보기
   
### Pet Clinic 과제풀이
1. first name 으로 검색하게 수정 (완)
   -> findOwner.html에서 값 바인딩 받아오기
   -> OwnerController에 바인딩 된 값 파람에 넣어서 더닞기
   -> OwnerRepository에 서비스 로직 수
2. key word 를 포함하고 있는 걸로 바꿔 보기 (완)
   -> @Query("SELECT DISTINCT owner FROM Owner owner left join fetch owner.pets WHERE owner.firstName LIKE CONCAT('%',:firstName,'%')")
   -> @Query("SELECT DISTINCT owner FROM Owner owner left join fetch owner.pets WHERE owner.firstName LIKE % :firstName%")
3. owner에 나이를 추가해 보기 (실패)   
    -> Owner 도메인 모델에 Age 추가 -> OK   
    -> 스키마와 Data 바꿔주시 -> Miss   
    => 에러로그 좀 잘 읽자
    => 그래도 Error
    => DB가 hsqldb가 아닌 h2 였어!!
    => 에러로그 좀 잘 읽자