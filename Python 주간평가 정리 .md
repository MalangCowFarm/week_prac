# 교재 1

모든 문자는 str 타입

### 문자열 연산

- 덧셈

```python
print("Hello" + "World") # HelloWorld 
```

- 곱셈

```python
print("Python" * 3) # PythonPythonPython
```

### 컨테이너

![](Python%20주간평가%20정리%20_assets/2023-02-05-20-17-30-스크린샷%202023-02-05%20오후%204.44.11.png)



- List(순서가 있는 구조로 저장)

![](Python%20주간평가%20정리%20_assets/2023-02-05-20-17-40-스크린샷%202023-02-05%20오후%204.47.39.png)

- 튜플
  
  -> List와 차이는 담고 있는 값 변경이 불가(불변 자료형)
  
  ![](Python%20주간평가%20정리%20_assets/2023-02-05-20-17-45-스크린샷%202023-02-05%20오후%204.49.28.png)

- 슬라이싱

![](Python%20주간평가%20정리%20_assets/2023-02-05-20-17-54-스크린샷%202023-02-05%20오후%204.59.04.png)

# 교재 2

### 조건문

- 조건문 예시

![](Python%20주간평가%20정리%20_assets/2023-02-05-20-18-00-스크린샷%202023-02-05%20오후%205.05.32.png)

-> 이런식으로 표주고 작성하라고 나올까바 그냥 넣어봄

![](Python%20주간평가%20정리%20_assets/2023-02-05-20-18-07-스크린샷%202023-02-05%20오후%205.36.06.png)

![](Python%20주간평가%20정리%20_assets/2023-02-05-20-18-11-스크린샷%202023-02-05%20오후%205.36.24.png)

- 딕셔너리 순회 및 Comprehension

![](Python%20주간평가%20정리%20_assets/2023-02-05-20-18-18-스크린샷%202023-02-05%20오후%205.38.13.png)

![](Python%20주간평가%20정리%20_assets/2023-02-05-20-18-46-스크린샷%202023-02-05%20오후%205.41.38.png)

- enumerate 순회
  
  -> 개인적으로 익숙치 않아서 넣음.
  
  ![](Python%20주간평가%20정리%20_assets/2023-02-05-20-18-31-스크린샷%202023-02-05%20오후%205.39.19.png)

![](Python%20주간평가%20정리%20_assets/2023-02-05-20-18-37-스크린샷%202023-02-05%20오후%205.40.17.png)



- Continue 및 for-else 문

![](Python%20주간평가%20정리%20_assets/2023-02-05-20-18-51-스크린샷%202023-02-05%20오후%205.43.04.png)

![](Python%20주간평가%20정리%20_assets/2023-02-05-20-18-57-스크린샷%202023-02-05%20오후%205.44.19.png)

# 교재 3

- filter

![](Python%20주간평가%20정리%20_assets/2023-02-05-20-19-05-스크린샷%202023-02-05%20오후%205.48.04.png)

 -> odd 함수를 numbers의 각 원소에 실행하고 결과값이 True( 1이상?)인 것들을 반환

- zip

![](Python%20주간평가%20정리%20_assets/2023-02-05-20-19-09-스크린샷%202023-02-05%20오후%205.50.22.png)

- lambda

![](Python%20주간평가%20정리%20_assets/2023-02-05-20-19-14-스크린샷%202023-02-05%20오후%205.52.46.png)

- 재귀함수
  
  -> 재귀함수를 이용한 팩토리얼
  
  ```python
  def factorial(n):
     if n == 0 or n == 1:
             return 1
       else:
             return n * factorial(n-1)
  print(factorial(4)) # 24
  ```
  
  -> 반복문을 이용한 팩토리얼

```python
def fact(n):
  result = 1
    while n>1:
          result *= n
          n -= 1
    return result

print(fact(4)) # 24
```

 -> 

    1. 재귀 호출은 입력 값이 커질 수록 연산 속도가 오래 걸림.
    1. 재귀 호출은 변수 사용을 줄여줄 수 있음.

- 패킹/언패킹 연산자

-> 패킹

```python
x, *y = 1, 2, 3, 4
print(x) # 1
print(type(x) # int
print(y) # [2, 3, 4]
print(type(y)) # list
```

```python
numbers = (1, 2, 3, 4, 5) # 패킹
print(numbers) # (1, 2, 3, 4, 5)
```

 -> 언패킹

```python
def multiply(x, y, z):
    return x * y * z
numbers = [1, 2, 3]
multiply(*numbers) # 6
```

```python
numbers = (1, 2, 3, 4, 5) # 패킹
a, b, c, d, e = numbers # 언패킹 (할당하려는 요수 갯수 동일 필수)
print(a, b, c, d, e) # 1, 2, 3, 4, 5
```

- 가변 키워드 인자

```python
def family(**kwargs):
    for key, value in  kwarngs.items():
        print(key, ':', value)
family(father='아부지', mother= '어무니', baby= '아기')
#father : 아부지
#mother : 어무니
#baby : 아기
```

## << 교재 4 는 관통pjt입니다. >>

# 교재 5

- 문자열 조회/탐색 및 검증 메서드

![](Python%20주간평가%20정리%20_assets/2023-02-05-20-19-23-스크린샷%202023-02-05%20오후%206.28.50.png)

```python
print('apple'.find('p')) # 1
print('apple'.find('p')) # -1
# find 는 오류가 없음
```

```python
print('apple'.index('p')) # 1
print('apple'.index('p')) # ValueError : substring not found
# index 는 오류가 발생함
```

- 문자열 변경 매서드

![](Python%20주간평가%20정리%20_assets/2023-02-05-20-19-28-스크린샷%202023-02-05%20오후%206.34.44.png)

- immutable인데 뭐시기 저시기~

![](Python%20주간평가%20정리%20_assets/2023-02-05-20-19-35-스크린샷%202023-02-05%20오후%206.36.01.png)

- 리스트 메서드

![](Python%20주간평가%20정리%20_assets/2023-02-05-20-20-14-스크린샷%202023-02-05%20오후%206.40.41.png)

# 교재 6

- 셋 메서드

![](Python%20주간평가%20정리%20_assets/2023-02-05-20-20-19-스크린샷%202023-02-05%20오후%206.42.25.png)

- 딕셔너리 메서드

![](Python%20주간평가%20정리%20_assets/2023-02-05-20-20-24-스크린샷%202023-02-05%20오후%206.43.15.png)

## <<교재 6은 관통pjt입니다.>>

# 교재 7

- 객체 비교

![](Python 주간평가 정리 _assets/image-20230205203216813-5601399.png)

- 클래스 변수와 인스턴스 변수

![image-20230205203258208](Python 주간평가 정리 _assets/image-20230205203258208.png)



# 객체 지향 프로그래밍

- 가방 두개를 만들기 위해 `물건을 넣고`, `뺄 수 있는` 가방의 형태를 만들고, `빨간색`을 입히고, `주머니`를 담아서 가방 하나를 만들고 다시, 가방의 형태를 만들고, `검정색`을 입히고, `꽃장식`을 달아야한다.
- 아래의 그림에서는 가방 공장에 `빨간색, 주머니 장식`과, `검정색, 꽃장식`을 요청하면 각각 완성된 가방이 나온다.

```python
class Bag: # 가방 공장
    def __init__(self, color, deco):
        self.color = color
        self.deco = deco
    def put(self, x):
        print(f"{x}를 가방에 넣었다.")
    def take_out(self, x):
        print(f"{x}를 가방에서 꺼냈다.")

hand_bag = Bag("red", "pocket") # 공장에서 만들어낸 생산품 -> 객체
shoulder_bag = Bag("black", "flower")

hand_bag.put("텀블러")
```

- 클래스 -> 공장

- 객체 -> 공장에서 만들어낸 생산품

- 객체 지향프로그래밍은 이러한 객체에 중심을 두어 프로그래밍하는 것

- 가방과 str

  - hand_bag이라는 객체
    - hand_bag의 속성 : 색깔 `red`, 장식 `pocket` -> 변수
    - hand_bag의 기능 : 물건을 넣기`put()`, 물건을 빼기`take_out()` -> 함수(메소드)
  - Bag(가방 공장)과 hand_bag(생산품)의 관계
    - 핸드백은 객체다
    - 핸드백은 Bag의 인스턴스다
    - 핸드백의 type이 Bag이다.

  ------

  - 'hello'라는 객체
    - hello의 속성 : 문자열 데이터 `'hello'`
    - hello의 기능 : 대문자로`upper()`, 알파벳으로 이루어져있는지 확인 `isalpha()`
  - str(문자열 공장)에서 만들어낸 'hello'(생산품)와의 관계
    - 'hello'는 객체다
    - 'hello'는 str의 인스턴스다
    - 'hello'의 type이 str이다

- 클래스 변수

![image-20230205210812168](Python 주간평가 정리 _assets/image-20230205210812168.png)



- 인스턴스 메서드

![image-20230205211038680](Python 주간평가 정리 _assets/image-20230205211038680.png)

-> 사실 저 위에 객체 지향 프로그래밍 예시만 보면 어느정도 개념이 잡힘

- 클래스 메서드 예시

![image-20230205211141154](Python 주간평가 정리 _assets/image-20230205211141154.png)

- 스태틱 메서드 예시

![image-20230205211234228](Python 주간평가 정리 _assets/image-20230205211234228.png)



# 교재 8

- 추상화

 -> 공통된 속성과 행위를 추출하는 것 불필요한 정보는 숨기고 중요한 정보만을 표현 -> 프로그램을 간단하게

![image-20230205211634413](Python 주간평가 정리 _assets/image-20230205211634413.png)

- 상속

-> 자식간의 관계와 유사(외모도 닮음) 하위 클래스는 상위 클래스의 속성, 메서드 등을 모두 상속받음 메서드 중복 사용 감소 -> 코드 효율적 / 재사용성 up 다중상속 -> 상속 순서에 의해 결정

![image-20230205211731299](Python 주간평가 정리 _assets/image-20230205211731299.png)

-> 다중상속 예시, 빨간박스가 상속 순서

![image-20230205211844892](Python 주간평가 정리 _assets/image-20230205211844892.png)

- 다형성

-> 다른 클래스의 객체들이 동일한 메시지에 대해 다른 방식으로 응답 메서드 오버라이딩  자식 클래스에서 같은 이름의 메서드로 덮어쓰기

![image-20230205211954651](Python 주간평가 정리 _assets/image-20230205211954651.png)

-> 매서드 오버라이딩

![image-20230205212022445](Python 주간평가 정리 _assets/image-20230205212022445.png)

- 캡슐화

-> 정보 보호 Public : 언더바 x 어디서나 호출 가능 Protected : 언더바 1개, 부모 자식클래스에서만 호출 가능 -> 확인은 가능 Private : 언더바 2개, 외부 호출 불가 -> getter setter 이용해야함

![image-20230205212128150](Python 주간평가 정리 _assets/image-20230205212128150.png)

-> public은 열린 대문, protacted는 닫혀있지만 노크하면 열리는 대문, private는 잠긴 대문 열쇠를 통해 열 수 있다.(내 주관적 비유임)

![](Python 주간평가 정리 _assets/image-20230205212306233.png)

- getter와 setter

![image-20230205212350717](Python 주간평가 정리 _assets/image-20230205212350717.png)

-> getter 는 호출되는 열쇠 기능, setter 는 안의 내용을 바꿀 수 있음.(또한 주관적 나의 생각)

- 간단한 클래스 예시

~~~python
class Overwatch:
    name = "감시기지 지브롤터"
    hero_count = 0

    def __init__(self, name, skill, ulti):
        self.name = name
        self.skill = skill
        self.ulti = ulti
        Overwatch.hero_count += 1
    
    def showInfo(self): # 인스턴스 메서드
        return (self.name, self.skill, self.ulti)
    
    @classmethod  # 클래스 메서드
    def map(cls):
        return f'{cls.name}에 오신 것을 환영합니다.'

    @staticmethod  # 스태틱 메서드
    def hi():
        return '안녕~!'


hero1 = Overwatch('Reinhardt', '돌진', '대지분쇄')  # 인스턴스 생성
hero2 = Overwatch('Genji', '질풍참', '용검')
hero3 = Overwatch('Mercy', '부활', '발키리')

# 클래스 변수
print(Overwatch.hero_count)  # 3

# 인스턴스 메서드
print(hero1.showInfo())  # ('Reinhardt', '돌진', '대지분쇄')
print(hero2.showInfo())  # ('Genji', '질풍참', '용검')
print(hero3.showInfo())  # ('Mercy', '부활', '발키리')

# 클래스 메서드
print(Overwatch.map())  # 감시기지 지브롤터에 오신 것을 환영합니다.

# 스태틱 메서드 - 인스턴스
print(hero1.hi())  # 안녕~!
print(hero2.hi())  # 안녕~!
print(hero3.hi())  # 안녕~!

# 스태틱 메서드 - 클래스
print(Overwatch.hi())  # 안녕~!
~~~

![2023-02-05-20-20-24-스크린샷 2023-02-05 오후 6.43.15](Python 주간평가 정리 _assets/2023-02-05-20-20-24-스크린샷 2023-02-05 오후 6.43.15.png)

