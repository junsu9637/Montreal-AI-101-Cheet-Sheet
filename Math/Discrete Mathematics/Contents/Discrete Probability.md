[1. 이산확률의 도입](#introduction-of-discrete-probabilities)          
[2. 확률론](#probability-theory)                 
[3. 베이즈 정리](#bayes-theorem)              
[4. 기댓값과 분산](#expected-values-and-variance)            
[예제](https://github.com/junsu9637/Study/blob/main/Math/Discrete%20Mathematics/Example/ACT7.md)

# Introduction of Discrete Probabilities

## 이산확률의 도입

확률 이론은 컴퓨터공학에서 다음과 같은 역할을 담당한다.
```markdown
1. 알고리즘 복잡도 계산
2. 결정론적 방식으로 해결 불가능한 문제 해결
3. 불확실성과 관련된 문제 해결
4. 현재 머신러닝 알고리즘의 핵심
```

> *확률은 '해당 사건이 일어나는 경우의 수 / 일어날 수 있는 모든 경우의 수'이다.*          
  -Laplace-

라플라스의 정의를 사용하기 위해서는 실험에서 일어날 수 있는 모든 경우의 수가 유한하고, 동일한 비율로 발생한다는 가정을 전제로 설정해야 한다.

## 유한 확률(Finite Probability)

> 실험(Experiment) : 일어날 수 있는 결과들의 집합을 발생시키는 과정
  표본공간(Sample space) : 일어날 수 있는 결과들의 집합
  사건(Event) : 표본공간의 부분집합
  
유한개의 일어날 수 있는 결과들이 포함된 사건의 확률에 대한 라플라스 정의는 다음과 같다.

> 동일한 비율로 발생할 수 있는 결과의 유한한 공집합이 아닌 표본공간 *S*와 *S*의 부분집합인 사건 *E*에 대한 *E*의 확률은 **P(E) = |E|/|S|** 이다.

사건 E는 표본공간 S의 부분집합이므로 확률은 음수이거나 1보다 클 수 없다.

## 여사건(Complementary event)

> 여사건 : S - E

여사건을 증명하면 다음과 같다.
```markdown
여사건 = S-E의 확률을 구하기 위해 |여사건| = |S|-|E|임을 사용할 수 있다.
P(여사건) = |S|-|E|/|S| = 1-|E|/|S| = 1-P(E)
```

## 합사건(Union event)

> 합사건 : P(E<sub>1</sub> U E<sub>1\2</sub>) = P(E<sub>1</sub>) + P(E<sub>1</sub>) - P(E<sub>1</sub> & E<sub>1\2</sub>)

## 확률적 추론(Probabilistic Reasoning)

# Probability Theory

## 확률론

앞서 확률을 정의할 때 모든 경우의 발생 가능성이 모두 같다고 정의했다. 그렇다면 발생 가능성이 같지 않은 실험의 경우에서 사건의 발생 가능성을 어떻게 모델링 할 것인가?

## 확률분포(Probability distribution)

표본공간 S의 확률을 P(s)라고 할 때, 다음의 조건을 만족해야 한다.
```markdown
1. 표본공간 S의 모든 s에 대하여 0<= P(s) <= 1
-> 각 경우의 확률이 0~1
2. P(s)의 총합 = P(E) = 1
-> 모든 결과의 확률의 총합 = 1
```
**확률분포**는 다음과 같은 조건을 만족한다.
> 표본공간 S의 모든 결과의 집합에 대한 함수 P

s가 n개일 때, s의 각 확률이 1/n으로 동일할 때의 확률분포를 **균등분포(Uniform distribution)** 이라고 한다.

적절한 확률분포 P(s)를 선택함으로써 발생 가능성이 같거나 다른 실험들을 모델링하는 것이 가능해진다.

## 여사건과 합사건의 확률

# Bayes Theorem

# Expected Values and Variance
