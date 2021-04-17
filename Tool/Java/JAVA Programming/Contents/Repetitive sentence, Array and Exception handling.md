[1. 반복문](#repetitive-sentence)        
[2. continue 문과 break 문](#continue-and-break)      
[3. 배열](#array)      
[4. 다차원 배열](#multy-array)         
[5. 메소드에서 배열 리턴](#return-array-in-method)            
[6. main() 메소드](#main-method)            
[7. 자바의 예외 처리](#exception-handling-of-java)           

# Repetitive sentence

## for 문

```Java
for (초기문; 조건식; 반복 후 작업) 
{
  //작업문
}

for(i=0; i<10; i++) 
{
  System.out.print(i);
} // 123456789
```

### 초기문

초기문은 다음과 같은 특징을 갖는다.
```markdown
1. 조건식에서 사용하는 변수를 초기화한다.
2. 시작할 때 한 번만 수행된다.
3. ,로 분리하여 여러 문장을 나열할 수 있다.
4. 빈 상태로 두어도 되지만 항상 ;은 있어야 한다.
```

다음과 같이 초기문에서 변수를 선언 할 수 있다. 하지만 이 변수는 **지역변수**로 for문에서만 사용 가능하다.
```Java
for(int i=0; ...) {} 
```

### 조건식

조건식은 다음과 같은 특징을 갖는다.
```markdown
1. 논리형 변수나 논리 연산을 사용한다.
2. 조건식 결과가 true면 반복되고 false면 벗어난다.
3. 조건식이 비어있거나 true면 무한 반복한다.
```

## while 문

```Java
while (조건식)
{
  // 작업문
}

while (i<10)
{
  System.out.print(i)
  i++
} // 123456789
```

## do-while 문
```Java
do
{
  // 작업문
} while(조건식);
```

do-while문은 while문과 다르게 조건식이 false더라도 작업문을 한 번 실행한다.

# Continue and Break

## continue 문

**continue 문**은 반복문을 빠져나가지 않으면서 즉시 다음 반복으로 넘어간다. 즉 다음과 같이 실행 경로만 변경되는 것이다.

![3.1](https://github.com/junsu9637/Study/blob/main/Tool/Java/JAVA%20Programming/Image/3_1.png?raw=true)

## break 문

**break 문**은 다음과 같이 하나의 반복문을 즉시 벗어난다.

![3.2](https://github.com/junsu9637/Study/blob/main/Tool/Java/JAVA%20Programming/Image/3_2.png?raw=true)

종종 while 문의 경우 조건식을 이용하여 while 문을 벗어나게 만들기 까다로운 경우가 많다. 이 때 다음과 같이 break 문을 사용한다면 간단하게 작성할 수 있다.
```Java
while ((n%5 ==0) || (n<0))
{
  ...
}

while(true)
{
  if(n%5 == 0) break;
  if(n<0) break;
}
```

# Array

## 배열

**배열**은 다음과 같이 같은 종류의 데이터들이 순차적으로 저장한다.
```Java
int i [] = new int[10];
// 이름 i인 10개의 정수 공간 배열 생성
```

이러한 배열은 다음과 같이 반복문을 통해 활용할 수 있다.
```Java
for (sum=0, n=0; n<10; n++)
{
  sum += i[n];
}
// 10개의 정수의 합을 구한다.
```

Java에서 배열의 생성은 C와는 다르게 다음과 같이 2단계로 이루어진다.
```markdown
1. 배열에 대한 레퍼런스 생성
2. 배열 생성 및 저장 공간 할당
```

위 내용을 코드로 확인해보면 다음과 같다.


```Java
int array [] = new int [5];

int array [];         // 배열에 대한 레퍼런스 변수 array 선언
array = new int [5];  // 배열 생성
```

## 배열 선언 및 생성


# Multy-Array
# Return Array in Method
# main-Method
# Exception handling-of-Java
