ⓒ JMC 2017

---

### 02 Random Variable

+ `확률변수 (random variable)` : 표본 공간에서 새롭게 정의되는 관심 대상
+ ex. 주사위 던지기 : 2개의 주사위 던졌을 때 나오는 결과보다 두 주사위의 합이 관심 대상일 수 있음

### 02 Expectation of RV

+ 확률변수 <img src="https://latex.codecogs.com/gif.latex?X"/>의 평균 <img src="https://latex.codecogs.com/gif.latex?E%5BX%5D"/>는 <img src="https://latex.codecogs.com/gif.latex?X%3Di"/>일 때의 확률값을 가중치로 곱한 값에 대한 '**가중 평균(weighted average)**'이다.
+ <img src="https://latex.codecogs.com/gif.latex?E%5BX%5D%20%3D%20%5Csum%20i%20%5Ccdot%20Pr%28X%3Di%29%20"/>

### 02 Linearity of Expectation

+ <img src="https://latex.codecogs.com/gif.latex?E%5BX+Y%5D%20%3D%20E%5BX%5D%20+%20E%5BY%5D"/>

### 02 확률분포 :: Bernoulli Distribution

+ 결과가 "성공success" 또는 "실패failure"로 나뉘는 확률변수의 분포
+ 확률변수 <img src="https://latex.codecogs.com/gif.latex?X"/> : 성공 여부
+ 성공: 1, 실패: 0

> **Note:** Bernoulli random variable = Indicator random variable

### 02 확률분포 :: Binomial Distribution

+ 결과가 확률 <img src="https://latex.codecogs.com/gif.latex?p"/>로 "성공"이거나 확률 <img src="https://latex.codecogs.com/gif.latex?1-p"/>로 "실패"인 <img src="https://latex.codecogs.com/gif.latex?n"/>번의 독립시행을 하는 확률변수의 분포
+ 확률변수 <img src="https://latex.codecogs.com/gif.latex?X"/> : <img src="https://latex.codecogs.com/gif.latex?n"/>번의 독립시행 중 성공 횟수
+ 확률질량함수 : <img src="https://latex.codecogs.com/gif.latex?p%28i%29%20%3D%20%5Cbinom%7Bn%7D%7Bi%7Dp%5E%7Bi%7D%281-p%29%5E%7Bn-i%7D"/>
+ 의미 : <img src="https://latex.codecogs.com/gif.latex?n"/>개 중에서 <img src="https://latex.codecogs.com/gif.latex?i"/>개를 선택하는 경우의 수

### 02 확률분포 :: Geometric Distribution

+ 확률 <img src="https://latex.codecogs.com/gif.latex?p"/>로 "성공"하는 독립시행을 성공이 나올 때까지 시행하는 확률변수의 분포
+ 확률변수 <img src="https://latex.codecogs.com/gif.latex?X"/> : 첫 성공이 나올 때까지 필요한 시행 횟수
+ 확률질량함수 : <img src="https://latex.codecogs.com/gif.latex?P%5C%7Bx%3Dn%5C%7D%20%3D%20%281-p%29%5E%7Bn-1%7Dp"/>

### 02 Example :: Binomial Distribution

```
Q. 어떤 항공사에서 탑승권 예약자의 5%가 탑승하러 오지 않음을 알았다.
이에 따라 50명의 승객을 태울 수 있는 항공편에 52개의 탑승권을 파는 정책을 쓴다.
탑승하러 나온 모든 승객에게 좌석배정이 가능할 확률은 얼마인가?
```

+ `예약자의 5%가 탑승하러 오지 않음` : "실패" 확률 (역: 95% = "성공" 확률)
+ `탑승하러 나온 모든 승객에게 좌석배정` : 선택하는 경우의 수
+ `52개의 탑승권을 가진 승객 중 50명에게 좌석배정` : <img src="https://latex.codecogs.com/gif.latex?n"/>개 중에서 <img src="https://latex.codecogs.com/gif.latex?i"/>개를 선택하는 경우의 수
  + <img src="https://latex.codecogs.com/gif.latex?%5Ctherefore"/> Binomial Distribution 문제

#### Solution :: Binomial Distribution

+ 확률변수 <img src="https://latex.codecogs.com/gif.latex?X"/>
  + 탑승하러 오는(="성공") 승객의 수
  + <img src="https://latex.codecogs.com/gif.latex?P%5C%7BX%3C%3D50%5C%7D"/>
+ 전체 시행 횟수와 성공 횟수
  + <img src="https://latex.codecogs.com/gif.latex?n%20%3D%2052"/>, <img src="https://latex.codecogs.com/gif.latex?i%20%3D%20%3C%3D%2050"/>
+ <img src="https://latex.codecogs.com/gif.latex?%5Ctherefore%201-P%28x%3D51%29-P%28x%3D52%29"/>


### 02 Example :: Geometric Distribution

```
Q. 공정한 동전을 연달아 던질 때 다섯 번째 시행에서 앞면이 처음으로 나올 확률은 얼마인가?
```

+ `공정한 동전` : 확률 <img src="https://latex.codecogs.com/gif.latex?1/2"/>로 "성공"하는 독립시행
+ `다섯 번째 시행에서 앞면이 처음으로 나온다` : 첫 앞면(="성공")이 나올 때까지 다섯번 시행한다
  + <img src="https://latex.codecogs.com/gif.latex?%5Ctherefore"/> Geometric Distribution 문제

#### Solution :: Geometric Distribution

+ 확률변수 <img src="https://latex.codecogs.com/gif.latex?X"/>
  + 첫 성공이 나올 때까지 필요한 시행 횟수
  + <img src="https://latex.codecogs.com/gif.latex?P%28X%3D5%29"/>
+ <img src="https://latex.codecogs.com/gif.latex?%5Ctherefore%20%281-1/2%29%5E%7B4%7D%20*%201/2"/>

### 02 Conditional Expectation

+ <img src="https://latex.codecogs.com/gif.latex?E%5BY%20%7C%20Z%3Dz%5D%20%3D%20%5Csum%20y%20%5Ccdot%20Pr%28Y%3Dy%20%7C%20Z%3Dz%29"/>
+ ex. 주사위 2개를 던질 때 첫 번째 주사위가 2가 나올 때 두 주사위의 합의 평균을 구하라
  + 두 주사위의 합 : 관심 대상이므로 확률변수 <img src="https://latex.codecogs.com/gif.latex?X"/>가 된다.
  + <img src="https://latex.codecogs.com/gif.latex?X%20%3D%20X_1%20+%20X_2"/>
  + <img src="https://latex.codecogs.com/gif.latex?E%5BX%20%7C%20X_1%20%3D%202%5D"/>

### 02 Conditional Expectation :: Lemma

+ 모든 확률변수 <img src="https://latex.codecogs.com/gif.latex?X"/>와 <img src="https://latex.codecogs.com/gif.latex?Y"/>에 대해서 다음이 성립한다.
+ <img src="https://latex.codecogs.com/gif.latex?E%5BX%5D%20%3D%20%5Csum%20Pr%28Y%3Dy%29%20%5Ccdot%20E%5BX%7CY%3Dy%5D"/>

### 02 Example :: Conditional Expectation

+ `@@@resume` married couples give births

---
