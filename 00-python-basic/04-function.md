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

파라미터에 기본값을 정해줄 수 있다.
당연히 파라미터의 오른쪽 끝에서부터 정해주어야 한다.

```python
def increment(num, step = 1):
    return num + step

print(increment(5, 3))
print(increment(5))
```

### 키워드 인자 (Keyword Argument)

함수 호출 시점에서 어떤 파라미터에 값을 넘겨줄 것인지
정해줄 수 있다는 것이다. 다음 코드는 `print()` 함수의
`end` 파라미터에 빈 문자열을 전달하여, 문자열 출력 후
줄바꿈 문자를 출력하지 않도록 하는 것이다.

```python
print('hello world', end='')
```

### 가변 인자 (VarArgs)

[A Byte of Python](https://python.swaroopch.com/functions.html)의 예제 코드로 설명을 대체한다.
알고리즘 풀면서 쓸 일은 별로 없을 것 같다.

```python
def total(a=5, *numbers, **phonebook):
    print('a', a)

    #iterate through all the items in tuple
    for single_item in numbers:
        print('single_item', single_item)

    #iterate through all the items in dictionary    
    for first_part, second_part in phonebook.items():
        print(first_part,second_part)

total(10,1,2,3,Jack=1123,John=2231,Inge=1560)
```

### 전역 스코프의 변수에 접근하기

```python
x = 50

def func(x):
    print('x is', x)
    x = 2
    print('Changed local x to', x)

func(x)
print('x is still', x)
```
```
$ python function_local.py
x is 50
Changed local x to 2
x is still 50
```

스코프 룰 자체는 C++와 비슷한 것 같다.
현재 스코프에서 변수를 찾을 수 없으면
차례대로 바깥 스코프로 이동하며 변수를 찾을 것이다.

다만 위 예제 코드에서 주의할 점은 `x = 2` 부분이다.
이는 전역 스코프에 있는 `x` 의 값을 변경하는 것이 아니라,
현재 스코프에서 `x` 라는 새로운 변수를 선언하고 2로 초기화하도록
동작한다.

만약 전역 스코프의 `x` 의 값을 변경하고 싶다면,
`global` 키워드를 사용할 수 있다.

```python
x = 50

def func():
    global x
    print('x is', x)
    x = 2
    print('Changed global x to', x)

func()
print('Value of x is', x)
```
```
$ python function_global.py
x is 50
Changed global x to 2
Value of x is 2
```

### 람다 함수