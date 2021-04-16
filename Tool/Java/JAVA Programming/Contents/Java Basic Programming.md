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
1. 특수문자(\_, $ 제외), 공백은 식별자로 사용 불가능
2. 자바 언어 키워드(if, while)는 식별자로 사용 불가능
3. 한글도 식별자로 사용 가능
4. 대소문자 구별
5. 길이 제한 없음
6. \_, $는 식별자 첫 번째 문자로 사용 가능하나 잘 사용하지 않음
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

![2.1]()

# Enter a key in Java
# Computation
# conditional sentence
