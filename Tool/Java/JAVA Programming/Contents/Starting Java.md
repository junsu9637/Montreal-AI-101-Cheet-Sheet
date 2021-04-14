[1. 컴퓨터와 프로그래밍](#conputer and programming)           
[2. 자바의 출현과 WORA](#emergence-of-java-and-wora)                
[3. 개발 도구와 자바 플랫폼](#development-tools-and-java-platforms#)                 
[4. 자바 프로그램 개발](#java-program-development)                
[5. 이클립스를 이용한 자바 프로그램 개발](#development-of-java-program-using-eclipse)                    
[6. 자바 언어의 활용](#use-of-java-language)             
[7. 자바의 특징](#characteristics-of-java)             

# Conputer and Programming

## 프로그래밍 언어

**프로그래밍 언어**는 컴퓨터가 실행한 프로그램을 작성하는 언어이다.

### 기계어
> 0,1의 이진수로 구성된 언어     
  컴퓨터의 CPU는 기계어만 처리가능
  
### 어셈블리어
> 기계어 명령을 니모닉 기호(표현하기 쉬운 상징적 단어)로 일대일 대응시킨 언어

### 고급언어
> 사람이 이해하기 쉽고, 벅잡한 작업, 자료구조. 알고리즘 등을 표현하기 위해 고안된 언어      
  절차 지향 언어와 객체 지향 언어로 나뉨

![1.1](https://github.com/junsu9637/Study/blob/main/Tool/Java/JAVA%20Programming/Image/1_1.png?raw=true)

## 프로그램 컴파일과 실행

프로그래밍 과정은 다음과 같다.
```markdown
1. 고급 언어로 프로그램 소스(프로그래밍 언어로 작성된 텍스트 파일) 파일 작성 
2. 컴파일 : 고급 언어를 기계어 코드로 변환
```

Java의 소스 프로그램 확장자는 **.java**이고, 자바 전용 컴파일러에 의해 **.class**로 컴파일된다. 클래스 파일은 **자바 가상 기계**에서 실행된다.
```markdown
Java : .java -> .class
C : .obj -> .exe
C++ : .cpp -> .obj -> .exe

# emergence of Java-and-wora

## 자바의 탄생

> 1991년 선마이크로시스템즈의 제임스 고슬링을 필두로 그린 프로젝트 시작      
  그린 프로젝트 : 가전 제품에 들어갈 소프트웨어 개발
  초기 이름 : Oak      
  웹 브라우저 Netscape에서 실행       
  인터넷과 웹의 발전으로 성장
  
> 1995년 Java로 발표
> 2009년 선마이크로시스템즈를 오라클에서 인수

### 자바의 목적

#### 플랫폼 호환성 문제 해결
> 기존 언어는 다른 종류 기기간의 호환성이 없었음
  소스를 다시 컴파일하거나 프로그램을 재 작성해야 했음
  
#### 플랫폼 독립적 언어 개발
> 모든 플랫폼에서 호환성을 갖는 프로그램 필요
  네트워크 및 웹에 최적화된 언어 필요
  
#### 메모리 사용량이 적고, 다양한 플랫폼 지원
> 내장형 시스템 요구 충족

## WORA(Write Once Run Anywhere)

Java는 한번 작성된 코드는 모든 플랫폼에서 바로 실행 가능한다. 이로 인해 기존 언어가 지녔던 플랫폼 종속성에서 벗어날 수 있게 되었다. 

*OS 및 H/W에 관계없이 동일하게 실행*

이러한 WORA는 **JVM(자바 가상 기계)** 와 **바이트 코드**로 인해 가능해졌다.

### 바이트 코드

```markdown
JVM애서만 실행되는 기계어 -> 자바 소스를 컴파일 하기위한 코드
CPU에 종석적이지 않음 -> 어느 CPU에서든지 코드 실행 가능
```

Java 코드 실행 과정
```markdown
자바 소스 프로그램 -> 바이트 코드의 클래스 파일
JVM에서 클래스 파일을 인터프리터 방식으로 실행
```

기존 언어들은 클래스 파일을 CPU가 직접 실행하기 때문에 CPU 종석적이지만 Java의 클래스 파일은 JVM에서 실행하기 때문에 CPU로부터 자유롭다.

### JVM(Java Virtual Machine)

**JVM(자바 가상 기계)** 는 자바 바이트 코드를 실행하는 소프트웨어다. 

## 플랫폼 종속성

> 플랫폼 = 하드웨어 플랫폼 + 운영체제 플랫폼

기존 언어는 컴퓨터 플랫폼에서 코드를 실행하기 때문에 플랫폼 종속적이다. 따라서 플랫폼이 바뀌면 코드를 실행할 수 없다. 하지만 Java는 컴퓨터 플랫폼이 아닌 


# Development Tools and Java Platforms

# Java Program Development

# Development of Java Program Using Eclipse

# Use of Java Language

# Characteristics of Java








```
