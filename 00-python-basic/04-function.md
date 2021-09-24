## 함수

### Python의 함수는

다음은 `map` 함수를 간단히 구현해본 것이다.

```python
def myMap(func, target):
    result = target[:]
    for i in range(len(result)):
        result[i] = func(result[i])
    return result

# output: [1, 4, 9]
print(myMap(lambda x: x**2, [1, 2, 3]))
```

위 코드를 관찰하여 알 수 있는 점은 다음과 같다.

- `def` 키워드를 통해 함수를 선언하고 있다.
- 리턴 타입과 파라미터 타입을 정의하지 않는다.
- `list` 타입의 객체를 리턴하도록 의도하고 있다.
  - 어떤 타입의 객체든 리턴할 수 있다.
- 함수를 파라미터로 받고 있다.
  - Python에서 함수는 일급 시민이다. 즉
  함수를 변수에 저장할 수 있으며,
  다른 함수의 파라미터로 함수를 넘기거나
  함수를 리턴하는 것도 가능하다.

### 디폴트 인자값 (Default Argument Value)

### 키워드 인자 (Keyword Argument)

### 가변 인자 (VarArgs)

### 전역 스코프의 변수에 접근하기

### 람다 함수