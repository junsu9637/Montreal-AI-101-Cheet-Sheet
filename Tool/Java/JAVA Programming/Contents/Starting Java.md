[1. 컴퓨터와 프로그래밍](#conputer-and-programming)           
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
```

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

**바이트 코드**는 JVM에서만 실행되는 기계어이다. 바이트 코드를 텍스트로 보기 위해서는 *디어셈블*이라는 과정을 거쳐야 한다.

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

기존 언어는 컴퓨터 플랫폼에서 코드를 실행하기 때문에 플랫폼 종속적이다. 따라서 플랫폼이 바뀌면 코드를 실행할 수 없다. 하지만 Java는 컴퓨터 플랫폼이 아닌 JVM이 실행하기 때문에 **플랫폼 종속성에서 자유롭다.**

기존 코드는 컴파일된 모든 코드를 *링커*를 통해 하나의 큰 실행 파일을 작성한다. 하지만 Java는 소스 코드를 각각의 바이트 코드로 작성한 후 필요한 상황에만 실행 파일로 사용한다. 따라서 기존 언어보다 **적은 메모리를 사용하여 작업을 수행할 수 있다.** 

![1.2](https://github.com/junsu9637/Study/blob/main/Tool/Java/JAVA%20Programming/Image/1_2.png?raw=true)

![1.3](https://github.com/junsu9637/Study/blob/main/Tool/Java/JAVA%20Programming/Image/1_3.png?raw=true)

## Java vs C/C++

### Java               
> 컴파일러가 바로 바이트 코드를 생성하며 링크 과정이 없다.       
  바이트 코드는 JVM에서만 실행 가능                      
  필요한 클래스들을 프로그램 실행 중에 동적 로딩               
>> 동적 로딩은 JVM에 포함된 클래스 로더에 의해 실행               
   ClassLoader 클래스를 이용하여 사용자가 직접 로딩 가능

### C/C++
> 목적 코드 및 실행 파일이 플랫폼에 따라 달라서 플랫폼이 바뀌면 소스 코드 수정                   
  컴파일러가 중간 단계인 목적코드 생성                 
  링커가 목적 코드와 라이브러리를 연결하고 실행 가능한 최종 실행 파일 생성                 
>> 정적 라이브러리 : 실행 파일에 포함시켜 실행 파일이 커짐          
   동적 라이브러리 : 실행 중 동적 링크

# Development Tools and Java Platforms

## JDK(Java Development Kit)

`개발도구 + JRE`

자바 개발자에게 무료로 제공하는 소프트웨어다. JDK를 설치하면 다음과 같은 파일이 설치된다.

> Java
>> jdk-(버전)
>>> bin : 자바 개발 및 실행에 필요한 도구와 유틸리티 명령
    donf : 여러 종류 배치 파일
    include : 네이티브 코드 프로그래밍에 필요한 C 언어 헤데 파일
    jmods : 컴파일된 모듈 파일
    legal : 각 모듈에 대한 저작권과 라이센스 파일
    lib : 실행 시간에 필요한 라이브러리 클래스

bin 디렉토리에 들어있는 주요 개발 소프트웨어들은 다음과 같다.

| 이름 | 실행 명령 |
|:-|:-|
| javac | 자바 컴파일러 : 자바 소스를 바이트 코드로 변환 |
| java | 자바 프로그램 실행기 : JVM을 작동시켜 자바 프로그램 실행 |
| javaodc | 자바 소스로부터 HTML 형식의 API 도큐먼트 생성 |
| jar | 자바 클래스 파일을 압축한 자바 아카이브 파일(.jar) 생성 및 관리 |
| jmod | 자바 모듈 파일(.jmod) 생성 및 오듈 파일의 내용 출력 |
| jlink | 응용프로그램에 맞춘 맞춤형 JRE 생성 |
| jdb | 디버거 : 자바 응용프로그램의 실행 중 오류를 찾는 데 사용 |
| javap | 디어셈블러 : 클래스 파일의 바이트 코드를 소스와 함께 보여줌 |

JDK는 여러 종류가 있는데 이를 **배포판** 이라고 부른다. 대표적인 배포판은 다음과 같다.

### Java SE(Standard Edition)

자바 표준 배포판으로 데스크탑과 서버 응용 개발 플랫폼이다.

### Java ME(Micro Edition)

모바일용 배포판으로 제한된 리소스를 갖는 하드웨어에서 응용 개발을 위한 플랫폼이다.

### Java EE(Enterprise Edition)
 
기업용 배포판으로 다중 사용자와 대규모 응용 개발을 위한 플랫폼이다.
 
## JRE

`Java API + JVM`

![1.4](https://github.com/junsu9637/Study/blob/main/Tool/Java/JAVA%20Programming/Image/1_4.png?raw=true)

# Java Program Development

# Development of Java Program Using Eclipse

# Use of Java Language

# Characteristics of Java








```
