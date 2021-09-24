## 제어문

### `if` 문으로 분기하기

```python
score = int(input())

if score >= 90:
    print('A')
elif score >= 80:
    print('B')
elif score >= 70:
    print('C')
else:
    print('D')
```

위 예제 코드만으로 충분히 설명을 대체할 수 있을 것 같다.  
`else if` 가 아닌 `elif` 키워드를 사용한다는 것을 기억하자.

참고로 Python에는 `switch` 문이 없다.

### `while` 문으로 반복하기

```python
n = 0
while n < 5:
    # if n == 3: break
    print(n)
    n += 1
else:
    print('loop ended')
```

`break` 및 `continue` 를 포함하여, Python의 `while` 은
C++와 크게 다르지 않다. 다만 반복문에 `else` 가 붙는다는 점은 재밌다.

`else` 블록은 반복 조건이 거짓이 되어 반복문이 종료되는 모든 경우에 실행된다.
다시 말하면, 반복 조건이 거짓이 되기 전에 임의로 `break` 하는 경우에는
`else` 블록이 실행되지 않는다는 것이다.
위 코드의 주석 부분을 uncomment하여 실행 결과를 비교해보면 알 수 있을 것이다.

참고로 Python은 반복문 라벨을 지원하지 않는다.

### `for` 문으로 반복하기

```python
for n in range(5):
    # if n == 3: break
    print(n)
    n += 1
else:
    print('loop ended')
```

`while` 문에서의 예제를 `for` 문으로 그대로 옮긴 것이다.
C++에서의 `for (int n: vec) {}` 문법과 닮았다.

`in` 다음에는
`list`, `dict`, `set`, `str`, `bytes`, `tuple`, `range` 등
Iterable한 타입의 객체가 위치해야 한다.
`for` 문은 해당 객체를 순회하며 원소를 하나씩 꺼내오는 동작을 수행한다.

참고로 `for` 문에서 원소를 꺼내오는 것은 기본적으로
배열의 해당 인덱스에 대한 참조가 아닌
원소 자체의 전달로 이루어진다.
C++에서의 `for (int &n: vec) {}` 와 같은 동작을 수행하지 않는다는 것이다.

`else` 문의 동작은 `while` 문에서의 설명과 같다.