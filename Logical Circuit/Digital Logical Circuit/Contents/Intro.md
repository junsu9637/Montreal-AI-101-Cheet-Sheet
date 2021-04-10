[1. 디지털과 아날로그](#digital-and-analog)                   
[2. 디지털 정보의 표현](#representation-of-digital-information)           
[3. 논리 레벨과 펄스파형](#logic-levels-and-pulse-waveforms)               
[4. 디지털 집적회로](#digital-integrated-circuit)                
[5. ADC와 DAC](#adc-and-dac)        
[예제](https://github.com/junsu9637/Study/blob/main/Logical%20Circuit/Digital%20Logical%20Circuit/Example/ACT1.md)

# Digital and analog

## 디지털신호와 아날로그 신호

### 아날로그 신호
>  자연계에서 일어나는 물리적인 양은 시간에 따라 연속적으로 변화            
   시간에 따라 연속적인 값을 갖음

### 디지털 신호
> 분명히 구별되는 두 레벨의 신호값 만을 갖음

## 디지털 시스템과 아날로그 시스템

### 시스템
> 임의 종합된 형태의 작업이나 기능을 수행하는 일정한 체계를 갖춘 기기의 집합체

### 아날로그 시스템
> 연속적인 정보를 입력받아 연속적인 형태의 정보를 출력하는 시스템

### 디지털 시스템
> 이산적인 정보를 가공하고 처리하여 최종 목적으로 하는 정보를 출력하는 시스템

아날로그 신호를 디지털 신호로 변환하기 위해서는 **아날로그-디지털 변환기(ADC)** 를 사용한다. 이를 통해 아날로그 시스템과 같은 대부분의 시스템들은 디지털 시스템으로 변환되어 사용한다. 디지털 시스템은 아날로그 시스템보다 다음과 같은 이점을 갖는다.

```markdown
1. 내, 외부 잡음에 강함
2. 설계하기 용의
3. 프로그래밍으로 전체 시스템을 제어할 수 있음 -> 변경에 쉽게 대응 -> 기능 구현의 유연성이 높음 -> 개발기간 단축
4. 정보 저장 및 가공 용의
5. 정보처리 정확성 및 정밀도 증가
6. 비선형 처리 및 다중화 처리 등 처리 가능
7. 전체 시스템 소형화 및 저가격화
```

대부분의 사람들이 익숙한 값은 아날로그 신호이기 때문에 궁극적으로는 아날로그 형태의 정보로 다시 변환해야 한다. 이를 위해 **디지털-아날로그 변환기(DAC)** 를 사용한다.


*디지털 시스템은 아날로그와의 인터페이스를 필요로 하기 때문에 전체 시스템을 효율적으로 구축하기 위해서는 아날로그 신호의 본질이나 특성을 이해해야한다.*

# Representation of digital information

## 디지털 정보의 전압레벨

디지털 정보를 표현하기 위해 2진수 체계를 사용한다. 사용하는 2진수 체계는 0과 1만의 2종류의 digit를 사용한다. 따라서 정보를 가장 간단한 형태로 나타낼 수 있다.

## 디지털 정보의 표현 단위

```markdown
1nibble = 4bit
1byte = 8bit
1byte = 1character
1word = CPU가 취급하는 명령어나 데이터 길이에 해당하는 bit
```

![1.1](https://github.com/junsu9637/Study/blob/main/Logical%20Circuit/Digital%20Logical%20Circuit/Image/1_1.png?raw=true)

비트는 0부터 시작을 한다. 가장 왼쪽에 있는 비트를 **MSB**, 가장 오른쪽에 있는 비트를 **LSB**라고 한다. 정보의 용량이 커지면 다음과 같이 **SI**, **IEC**를 따른다.

![1.2](https://github.com/junsu9637/Study/blob/main/Logical%20Circuit/Digital%20Logical%20Circuit/Image/1_2.png?raw=true)

컴퓨터의 성능이 발전하면서 다룰 수 있는 정보의 용량이 증가하면서 SI와 IEC간의 오차 또한 증가한다. 따라서 IEC 60027-2에 정의된 정확한 단위를 사용해야 한다.

# Logic levels and Pulse waveforms

## 정논리와 부논리

디지털 논리 시스템은 보통 전압이 가해지고 있는 상태(HIGH 레벨)을 1이라고 표현하고, 전압이 가해지고 있지 않은 상태(LOW 레벨)을 0이라고 표현한다.

**정논리(=양논리)** 는 HIGH 레벨을 1이라고 표현하는 방식이고, **부논리(=음논리)** 는 LOW 레벨을 1이라고 표현하는 방식이다.

## 펄스 파형

### 펄스
전압 레벨이 HIGH와 LOW 상태를 반복하는 상태로 **주기 펄스**와 **비주기 펄스**로 나뉜다. 주기 펄스는 일정한 구간마다 파형이 반복되고, 비주기 펄스는 주기가 없다.

이상적인 펄스 파형은 다음과 같다.

![1.3](https://github.com/junsu9637/Study/blob/main/Logical%20Circuit/Digital%20Logical%20Circuit/Image/1_3.png?raw=true)

이상적인 펄스 파형은 두 개의 에지(상승에지, 하강에지)로 구성된다. 상승에지는 리딩 에지, 하강에지는 트레일링 에지라고도 한다.

하지만 실제적인 펄스 파형은 다음과 같다.

![1.4](https://github.com/junsu9637/Study/blob/main/Logical%20Circuit/Digital%20Logical%20Circuit/Image/1_4.png?raw=true)

상승 시간은 LOW 레벨에서 HIGH 레벨로 증가하는데 걸리는 시간이고, 하강 시간은 HIGH 레벨에서 LOW 레벨로 감소하는데 걸리는 시간을 의미한다.
실제로는 진폭이 10%에서 90%까지 증가하는 시간을 상승 시간으로 정의하고 진폭이 90%에서 10%로 감소하는 시간을 하강 시간이라고 정의한다. 펄스 폭은 상승 구간과 하강 구간의 50%인 두 지점 사이 시간 간격으로 정의한다.

## 주기, 주파수, 및 듀티 사이클

### 주파수
> 주기적인 파형이 1초 동안에 진동한 횟수
  주파수와 주기는 역수 관계
  
### 듀티 사이클

듀티 사이클은 충격 계수라고도 하는데 주기적인 펄스파형의 특성을 반영한다. 듀티 사이클은 다음과 같이 정의된다.

> duty cycle = t<sub>w</sub>/T * 100%

# Digital Integrated Circuit

### 디지털 회로
> 디지털 정보를 처리하는 디지털 시스템의 하드웨어           
  2진 상태와 회로를 구성하는 논리에 따라 반응하여 2진 상태의 출력 신호 발생
  
### 조합논리회로
> 기본 게이트(저항, 다이오드, 트랜지스터)의 조합으로 구성되는 논리회로

### 순서논리회로
> 조합논리회로에 입력과 출력 신호를 기억하는 플립플롭 또는 메모리를 부가
  논리 신호가 순차적으로 발생 

### 집적회로
> 실리콘 칩 위에 저항, 커패시터, 다이오드, 트랜지스터 등의 상호연결

## IC 패키지

PCB에 장착하는 방법에 따라 **삽입 장착형**과 **표면 실장형**으로 구분한다.

### PCB

> 위에 칩이나 기타 전자부품들이 설치되어 있는 판      
  시스템보드 또는 마더보드라고 부른다

### 삽입 장착형 IC
> PCB 보드의 구명에 끼우는 핀을 가지고 있어 뒷면의 도체에 납땜으로 연결할 수 있다
  DIP 형태를 갖는다
  
### 표면 실장형 IC
> PCB 표면에 금속 처리된 곳에 직접 납땜 처리

![1.5](https://github.com/junsu9637/Study/blob/main/Logical%20Circuit/Digital%20Logical%20Circuit/Image/1_5.png?raw=true)

### DIP
> 집적회로에 가장 널리 사용되는 핀 배열 
  집적회로 양쪽 면에 두 개의 직선으로 정렬
  
### SOIC
> DIP의 리드 간격을 절반으로 줄이고, 리드는 표면 실장을 위해 구부러짐

### QFP
> 리드가 4방향으로 나온 SOIC

### PLCC
> 리드 끝부분이 J형으로 구부러짐

### SMD
> 기판에 직접 납땜하는 집적회로
  장치 제거가 어려움
  DIP 크기의 70%, 무게의 90% 감소로 인한 제조 가격 하락

### 디지털 시스템의 장점
```markdown
1. 소형화 및 경량화
2. 생산가격 저렴화
3. 소비전력 감소
4. 동작속도 고속화
5. 신뢰도 상승
```

## 집적회로의 분류

![1.6](https://github.com/junsu9637/Study/blob/main/Logical%20Circuit/Digital%20Logical%20Circuit/Image/1_6.png?raw=true)

# ADC and DAC

다음과 같은 장점으로 인해 아날로그 신호를 디지털 신호로 변환하여 처리한다.
```markdown
1. 디지털 회로를 통한 신호처리가 잡음의 영향을 덜 받고, 신뢰도 높음
2. 정보 저장 가능 및 대규모 IC화 용이
```

> **아날로그-디지털 변환기(ADC)** : Analog-to-Digital-Converter           
  **디지털-아날로그 변환기(DAC)** : Digital-to-Analog-Converter

따라서 **아날로그-디지털 변환기(ADC)** 를 통해 아날로그 신호를 디지털 신호로 변환한다. 변환은 다음과 같이 이루어진다.

![1.7](https://github.com/junsu9637/Study/blob/main/Logical%20Circuit/Digital%20Logical%20Circuit/Image/1_7.png?raw=true)

## 표본화

![1.8](https://github.com/junsu9637/Study/blob/main/Logical%20Circuit/Digital%20Logical%20Circuit/Image/1_8.png?raw=true)

아날로그 신호를 디지털 신호로 변환하기 위해서는 일정한 간격으로 표본화를 진행해야 한다.

### 샤논의 표본화 정리
> 신호의 최고 주파수의 2배 이상의 빈도로 샘플링하면 샘플링된 데이터로부터 본래 데이터를 재현 가능하다

## 양자화

![1.9](https://github.com/junsu9637/Study/blob/main/Logical%20Circuit/Digital%20Logical%20Circuit/Image/1_9.png?raw=true)

펄스의 진폭 크기를 디지털 양으로 변환해야 한다. 이 과정에서 불가피한 **양자화 잡음**이 발생한다. 양자화 잡음은 미리 정한 신호레벨의 수를 늘려 줄일 수 있으나 데이터의 양이 많아진다.

## 부호화

![1.10](https://github.com/junsu9637/Study/blob/main/Logical%20Circuit/Digital%20Logical%20Circuit/Image/1_10.png?raw=true)

양자화한 값을 2진 디지털 부호로 변환해야 한다. 일반적으로 음성에서는 8비트로 부호화를 수행한다.

전체 과정은 다음과 같이 수행된다.
![1.11](https://github.com/junsu9637/Study/blob/main/Logical%20Circuit/Digital%20Logical%20Circuit/Image/1_11.png?raw=true)

## ADC와 DAC

![1.12](https://github.com/junsu9637/Study/blob/main/Logical%20Circuit/Digital%20Logical%20Circuit/Image/1_12.png?raw=true)
