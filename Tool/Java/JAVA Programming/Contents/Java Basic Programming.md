[1. 자바 프로그램의 구조](#structure-of-the-java-program)      
[2. 식별자](#identifier)      
[3. 자바의 데이터 타입](#data-type-of-java)      
[4. 자바에서 키 입력](#enter-a-key-in-java)      
[5. 연산](#computation)      
[6. 조건문](#conditional-sentence)     

# Structure of the Java program

## 클래스 만들기
```Java
public class Hello
{
  // 내용
}
```

## 주석문
```Java
// 한 라인 주석으로 행을 주석 처리

/*
여러 라인을 주석 처리 (/* */)
............................
*/
```

## main() 메서드
```Java
public static void main(String[] args)
{
  // 내용
)
```
> main() 메서드는 한 클래스에 2개 이상 작성되면 안된다.       
  반드시 public, static, void 타입으로 선언되어야 한다 

## 메서드
메서드 작성
```Java
public static int sum(int n, int m) // 매개변수 n, m
{
  return n+m;
}
```

메서드 호출
```Java
s = sum(10 ,20);
```

## 변수 선언
```Java
int i; // 변수 선언
int j = 1; // 변수 선언과 동시에 초기화
```

## 화면 출력
```Java
System.out.print("a") // 내용 화면 출력
System.out.println("a") // 화면 출력 후 다음 행 이동
```

# Identifier

## 식별자 이름 규칙
```markdown
1. 특수문자(_, $ 제외), 공백은 식별자로 사용 불가능
2. 자바 언어 키워드(if, while)는 식별자로 사용 불가능
3. 한글도 식별자로 사용 가능
4. 대소문자 구별
5. 길이 제한 없음
6. _, $는 식별자 첫 번째 문자로 사용 가능하나 잘 사용하지 않음
```

## 좋은 이름
프로그램 가독성을 높이기 위한 이름을 결정하는 방법은 다음과 같다.
```markdown
1. 목적에 맞는 이름
2. 충분히 긴 이름
3. 언어 관습을 따르는 이름
```

### 클래스 이름
```Java
class HelloWorld {}
/* 
클래스 이름의 첫 번째 문자는 대문자
여러 단어가 복합되면 각 단어 첫 번쨰 문자가 대문자
*/
```

### 변수, 메서드 이름
```Java
int myAge;
public int getAge() {} 
/*
클래스와 구별하기 위해 첫 번째 문자는 소문자
여러 단어가 복합되면 두 번째 단어부터 첫 번째 문자가 대문자
*/
```

### 상수 이름
```Java
final double PI = 3.14; 
// 모든 문자는 대문자
```

# Data type of Java

## 기본 타입

자바 기본 타입의 크기가 정해져 있기 때문에 CPU나 운영체제에 따라 변하지 않는다.

![2.1](https://github.com/junsu9637/Study/blob/main/Tool/Java/JAVA%20Programming/Image/2_1.png?raw=true)

## 문자열
```Java
String name = "junsu";
```

## 리터럴

프로그램에 직접 표현한 값

### 정수 리터럴
```Java
int n = 15;       // 15
int m = 015;      // 015 = 14
int k = 0x15;     // 0x15 = 21
int b = 0b0101;   // 0b0101 = 5
long g = 1L; // long은 리터럴 뒤에 L 또는 l을 추가
```

### 실수 리터럴
```Java
double d = 0.1234;
double e = 1234E-4; // 1234E-4 = 1234*0.0001 = 0.1234
float f = 0.1234f;    // F나 f를 붙이면 float
double w = 0.1234d;   // D나 d를 붙이면 double
```

### 문자 리터럴
```Java
char a = 'A'
char b = \u0041 // 문자 'A'의 유니코드 값
char c = '글' 
char d = \uae00 // 문자 '글'의 유니코드 값
```

### 논리 리터럴
```Java
boolean a = true;
boolean b = 10 > 0; // true
```

### 특수문자 리터럴
| 종류 | 의미 | 종류 | 의미 |
|:-:|:-|:-:|:-|
| \b | 백스페이스 | \r | 캐리지 리턴 |
| \t | 탭 | \" | 이중 인용부호 |
| \n | 라인피드 | \' | 단일 인용부호 |
| \f | 폼피드 | \\ | 백슬래쉬 |

### null 리터럴
```Java
int n = null; // 기본 타입에 null 값을 지정할 수 없음
String str = null;
```

### var 키워드
var을 사용하면 다음과 같이 자동으로 타입을 결정할 수 있다.
```Java
var a = 200;       // a는 int 타입으로 결정
var b = "asd";     // b는 String 타입으로 결정
var c = 3.14;      // c는 double 타입으로 결정
var d = new d();   // d는 d 타입으로 결정
var e;             // 오류. 초깃값 없이 사용 불가능
```

var은 지역 변수에서만 사용할 수 있다.

var은 초깃값이 주어지지 않으면 사용할 수 없다.

## 상수

상수 선언을 위해서는 변수 선언에서 **final**을 추가하면 된다.
```Java
final double PI = 3.14;
```

상수는 한번 설정하면 변경할 수 없다.

## 타입 변환

### 자동 타입 변환

수식 내에서 타입이 일치하지 않을 때, 컴파일러가 자동으로 **작은 타입을 큰 타입으로 자동 변환**한다.

```Java
long m = 25         // int 타입 25 -> long 타입 25
double d = 3.14*10; // 연산을 위해 10 ->10.0
```

### 강제 타입 변환

다음과 같이 ()통해 강제로 형변환을 시킨다. 강제 형변환을 **캐스팅**이라고 부른다.

```Java
int n = 100;
byte b = (byte)n;
```

# Enter a key in Java

## System.in

**System.in**은 키보드 장치를 직접 제어하고 입력을 받는 **표준 입력 스트림** 객체다. 

다음과 같이 키 값을 바이트 데이터로 넘겨주므로 응용프로그램이 문자 정보로 변환해야 한다.

![2.2](https://github.com/junsu9637/Study/blob/main/Tool/Java/JAVA%20Programming/Image/2_2.png?raw=true)

## Scanner 클래스
**Scanner**은 응용프로그램이 키 입력을 쉽게 받을 수 있는 패키지다. 

### import 문 사용

Scanner를 사용하기 위해서는 다음과 같이 java.util 패키지에 있는 Scanner을 import해야한다.
```Java
import java.util.Scanner;
```

### Scanner 객체 생성

다음과 같이 Scanner 객체를 생성한다.

```Java
Scanner scanner = new Scanner(System.in);
```

생성문은 다음과 같은 구조로 진행된다. scanner 객체는 System.in 객체를 이용해서 키보드로부터 바이트 정보들을 입력 받는다. 이 바이트들을 응용프로그램이 적절한 타입으로 변환하여 리턴한다.

![2.3](https://github.com/junsu9637/Study/blob/main/Tool/Java/JAVA%20Programming/Image/2_3.png?raw=true)

### Scanner 클래스로 키 입력받기

Scanner 클래스는 키 값을 공백 문자를 기준으로 분리하여 **토큰 단위**로 읽는다. Scanner 클래스로 키를 입력받으면 다음과 같다. 

```Java
Scanner sc = new Scanner(System.in); // Kim Seoul 20 65.1 true 입력 
String name = sc.next();             // Kim
String city = sc.next();             // Seoul
int age = sc.nextInt();              // 20
double weight = sc.nextDouble();     // 65.1
boolean isSingle = sc.nextBoolean(); // true
```

추가적인 메소드는 다음과 같다.

![2.4](https://github.com/junsu9637/Study/blob/main/Tool/Java/JAVA%20Programming/Image/2_4.png?raw=true)

# Computation

자바에는 다음과 같은 식 연사자들이 존재한다.

![2.5}()

## 연산자 우선순위

다음은 연산자 우선순위로 ()는 최우선순위를 갖는다.

![2.6]()

## 산술 연산자

산술 연산자는 다음과 같다.

![2.7]()

## 증감 연산자

증감 연산자는 다음과 같다.

![2.8}()

```Java
// 전위 연산자
a = 1;
b = ++a; // a=2, b=2

// 후위 연산자
a = 1;
b = a++; // a=2, b=1
```

## 대입 연산자

대입 연산자는 다음과 같다.

![2.9]()

## 비교 연산자

비교 연산자는 다음과 같다.

![2.10]() 

## 논리 연산자

논리 연산자는 다음과 같다.

![2.11]()

## 조건 연산자

**조건 연산자**는 3개의 피연산자로 구성되어 **삼항 연산자**라고도 불린다. 다음 두개의 코드는 같은 코드다.

```Java
int s = (x>y) ? 1 : -1;
```
```Java
int s;
if (x>y)
{
  s = 1;
}
else
{
  s = -1;
}
```

## 비트 연산자

비트 연산자는 다음과 같다.

![2.12]()

![2.13]()

> \>\> 는 1비트 쉬프트 할 때마다 2로 곱하거나 나누기 때문에 **산술적 시프트**라고 부른다.
  \>\>\>는 항상 최상위 비트에 0이 삽입되어 나누는 효과가 나타나지 않아 **논리적 시프트**라고 부른다.

# conditional sentence
