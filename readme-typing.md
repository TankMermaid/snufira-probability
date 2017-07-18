ⓒ JMC 2017

---

### 02 Random Variable

+ `확률변수 (random variable)` : 표본 공간에서 새롭게 정의되는 관심 대상
+ ex. 주사위 던지기 : 2개의 주사위 던졌을 때 나오는 결과보다 두 주사위의 합이 관심 대상일 수 있음

### 02 Expectation of RV

+ 확률변수 $X$의 평균 $E[X]$는 $X=i$일 때의 확률값을 가중치로 곱한 값에 대한 '**가중 평균(weighted average)**'이다.
+ $E[X] = \sum i \cdot Pr(X=i) $

### 02 Linearity of Expectation

+ $E[X+Y] = E[X] + E[Y]$

### 02 확률분포 :: Bernoulli Distribution

+ 결과가 "성공success" 또는 "실패failure"로 나뉘는 확률변수의 분포
+ 확률변수 $X$ : 성공 여부
+ 성공: 1, 실패: 0

> **Note:** Bernoulli random variable = Indicator random variable

### 02 확률분포 :: Binomial Distribution

+ 결과가 확률 $p$로 "성공"이거나 확률 $1-p$로 "실패"인 $n$번의 독립시행을 하는 확률변수의 분포
+ 확률변수 $X$ : $n$번의 독립시행 중 성공 횟수
+ 확률질량함수 : $p(i) = \binom{n}{i}p^{i}(1-p)^{n-i}$
+ 의미 : $n$개 중에서 $i$개를 선택하는 경우의 수

### 02 확률분포 :: Geometric Distribution

+ 확률 $p$로 "성공"하는 독립시행을 성공이 나올 때까지 시행하는 확률변수의 분포
+ 확률변수 $X$ : 첫 성공이 나올 때까지 필요한 시행 횟수
+ 확률질량함수 : $P\{x=n\} = (1-p)^{n-1}p$

### 02 Example :: Binomial Distribution

```
Q. 어떤 항공사에서 탑승권 예약자의 5%가 탑승하러 오지 않음을 알았다.
이에 따라 50명의 승객을 태울 수 있는 항공편에 52개의 탑승권을 파는 정책을 쓴다.
탑승하러 나온 모든 승객에게 좌석배정이 가능할 확률은 얼마인가?
```

+ `예약자의 5%가 탑승하러 오지 않음` : "실패" 확률 (역: 95% = "성공" 확률)
+ `탑승하러 나온 모든 승객에게 좌석배정` : 선택하는 경우의 수
+ `52개의 탑승권을 가진 승객 중 50명에게 좌석배정` : $n$개 중에서 $i$개를 선택하는 경우의 수
  + $\therefore$ Binomial Distribution 문제

#### Solution :: Binomial Distribution

+ 확률변수 $X$
  + 탑승하러 오는(="성공") 승객의 수
  + $P\{X<=50\}$
+ 전체 시행 횟수와 성공 횟수
  + $n = 52$, $i = <= 50$
+ $\therefore 1-P(x=51)-P(x=52)$


### 02 Example :: Geometric Distribution

```
Q. 공정한 동전을 연달아 던질 때 다섯 번째 시행에서 앞면이 처음으로 나올 확률은 얼마인가?
```

+ `공정한 동전` : 확률 $1/2$로 "성공"하는 독립시행
+ `다섯 번째 시행에서 앞면이 처음으로 나온다` : 첫 앞면(="성공")이 나올 때까지 다섯번 시행한다
  + $\therefore$ Geometric Distribution 문제

#### Solution :: Geometric Distribution

+ 확률변수 $X$
  + 첫 성공이 나올 때까지 필요한 시행 횟수
  + $P(X=5)$
+ $\therefore (1-1/2)^{4} * 1/2$

### 02 Conditional Expectation

+ $E[Y | Z=z] = \sum y \cdot Pr(Y=y | Z=z)$
+ ex. 주사위 2개를 던질 때 첫 번째 주사위가 2가 나올 때 두 주사위의 합의 평균을 구하라
  + 두 주사위의 합 : 관심 대상이므로 확률변수 $X$가 된다.
  + $X = X_1 + X_2$
  + $E[X | X_1 = 2]$

### 02 Conditional Expectation :: Lemma

+ 모든 확률변수 $X$와 $Y$에 대해서 다음이 성립한다.
+ $E[X] = \sum Pr(Y=y) \cdot E[X|Y=y]$

### 02 Example :: Conditional Expectation

+ `@@@resume` married couples give births

---
