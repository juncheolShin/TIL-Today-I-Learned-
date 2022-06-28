# Vectorization

벡터화는 코딩에서 명시적인 for루프를 제거하는 기술임   
벡터화된 것이 훨씬 빠름 -> 데이터셋이 커질수록 시간 절약


### Non-Vectiorized Version
$ z = w^{^{t}}x + b $
```
z = 0
for i in range(n-x) :
  z += w[i] * x[i]
z += b
```

### Vectorized Version
```
z = np.dot(w,x) + b
```
> np.dot(w,x) = $w^{^{t}}x$
> > np = numpy


