## Python 기초

알고리즘 문제 풀이를 위한 최소한의 Python 문법을 공부합니다.  
기존에 다른 프로그래밍 언어, 특히 C++의 문법을 알고 있다고 가정합니다.

### 시작하기 전에

```python
print('hello world!')
```

- Python2와 Python3의 문법에는 차이가 있다.
  - 본 문서는 Python3의 문법을 기준으로 한다.
  - 터미널에서 `python` 명령어를 실행했을때 Python2가 실행된다면, `python3` 명령어를 사용하자.
- C++에서 중괄호를 통해 블록을 구분하는 것과 달리, Python은 들여쓰기로 블록을 구분한다.
- 현재로서 Python은 분명히 C++보다 느린 언어이다.
  - 때문에 코딩 테스트가 아닌 알고리즘 대회의 경우는 아무래도 C++를 사용하는 것이 유리할 것이다.
  - BOJ의 경우, `(C/C++ 시간 제한)*3+2` 만큼의 시간 제한 보너스가 적용된다. 다만 '추가 시간 없음'이라고 명시된 경우는 보너스가 없기 때문에, Python을 포기하자.
  - 일반적으로 Pypy3가 Python3보다 실행 속도가 빠르다. BOJ에서 Python3대신 Pypy3로 제출할 수 있다.
- BOJ에서 Python 사용시 유의할 사항은 다음 링크를 참고한다. https://www.acmicpc.net/blog/view/70


### 목차

1. [입출력](01-io.md)
2. [연산자](02-operator.md)
3. [제어문](03-control-flow.md)
4. [함수](04-function.md)
5. [유용한 내장 함수들](05-builtin-function.md)
6. [자료구조 하나: Python 기본 자료구조](06-data-structure-1.md)
7. [자료구조 둘: Python 기본 자료구조의 시간 복잡도](07-data-structure-2.md)

### 참고자료

[A Byte of Python](https://python.swaroopch.com/)