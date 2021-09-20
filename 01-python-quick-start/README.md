## Python Quick Start

알고리즘 문제 풀이를 위한 최소한의 Python

### 들어가기 전에

### 콘솔 입출력

### 기본 자료형

### 문자열 다루기

### 연산자

| 연산자 | 설명 |
| :---: | :---: |
| `+` `-` `*` `/` | 사칙 연산. 나눗셈 결과는 실수형. |
| `//` | 나눗셈 & 버림. 정수 결과를 반환. |
| `**` | 거듭제곱 |
| `%` | 모듈러 연산 |
| `=` `+=` `-=` `*=` `/=` `//=` `**=` `%=` | 대입 연산 |
| `&` `\|` `^` `~` | 비트 연산 |
| `<<` `>>` | 비트 시프트 연산 |
| `<` `>` `<=` `>=` `==` `!=` | 비교 연산 |
| `not` `and` `or` | 논리 연산 |
| `in` `not in` | 멤버십 연산 |
| `is` `is not` | 참조 비교 연산 |

### 제어문

__`if` 문__

```python
score = 93

if score >= 95:
  print('A+')
elif score >= 90:
  print('A')
else:
  print('B+')
```

- 키워드 : `if`, `elif`, `else`
- Python에는 `switch`가 없음.

__`while` 문__

```python
i = 0
while i < 5:
  print(i)
  i += 1
else:
  print('end')
```

- 반복문에 `else`?
  - 반복 조건이 False가 되어 탈출하는 모든 경우에 `else` 블록이 실행됨
  - 다시 말하면, `break`로 인해 반복 조건이 `False`가 되기 전 탈출하면 `else` 블록은 실행되지 않음

__`for` 문__

```python
for i in range(0, 5):
  print(i)
else:
  print('end')
```

- C++에서 제공하는 `for (int i: vec) {}` 문법과 비슷
- `range(0, 5)`는 0 이상 5 미만의 정수 리스트를 반환. 정확히는 리스트가 아닌 `range` 객체. Step을 지정하는 등 더 많은 기능이 있음
- `range`를 포함해 모든 Iterable한 객체가 `in` 뒤에 들어갈 수 있는 듯
- `else`는 `while`과 같음

### 함수

### 심화 자료형