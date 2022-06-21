# Logistic Regression as a neural network

## Binary Classification
신경망에서 학습 데이터를 x, 결과를 y로 표기하고 y = 0,1 의 값을 가짐(True,False)        
이때 한 데이터-결과 세트를 (x,y)로 표기함.

## Losgistic Regression
```
y 값의 0,1 인 경우, 즉 Binary Classification 문제에서 사용하는 알고리즘
```
x 가 주어졌을 때 , $\hat{y}$ 을 구함. 
>$\hat{y}$ = x가 주어졌을 때 y=1이 될 가능성.

```
입력값이 x이고 parameter가 W, b인 경우 y-hat을 어떻게 구할까?
(W = x차원 벡터, b = 실수)
```

가장 간단한 방법 : $W \times transpose \times x + b$
>하지만 이 방법은 값이 음수이거나 1이상으로 나올 수 있음.   
>값이 0에서 1사이로 결정되기 위한 방법 : Sigmoid

sigmoid 함수를 위 식 앞에 붙여서 $\hat{y}$을 구함.

Sigmoid Function : $S(x) = \frac{1}{1+e^{-x}}$

## Logistic Regression Cost Function
* 가장 간단한 손실함수   
Loss (error) Function : $L(y,\hat{y}) = \frac{(\hat{y} - y)^2}{2}$
```
하나의 볼록한 함수면 괜찮다. 다만 울퉁불퉁한 개형이 나온다면 최저점을 찾기 힘듬. 
```
$\to$ 실제로 사용하는 함수 
Loss (error) Function : $$L(y,\hat{y}) = - (y\log{}{\hat{y}} + (1-y)\log{}{(1-\hat{y})})$$

* Cost Function : 모든 손실함수의 평균   
$J(W,b) = \frac{\displaystyle\sum_{i=1}^{m}L(\hat{y},y)}{m}$
