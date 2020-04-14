# 1. 클래스

## 1.1. Random 클래스

### 1.1.1. 생성

```c#
Random random = new Random();
```

random 변수 생성.

### 1.1.2. 메서드

> - `Next()` : int 크기의 0~maxValue 를 출력.[^int]
> - `Next(a, b)` : a 부터 b 만큼의 숫자를 출력.[^int]
> - `NextDouble()`  : 0.0 과 1.0 사이의 난수를 반환[^double]

```c#
using System;

namespace ConsoleApp1
{
    class Program
    {
        static void Main(string[] args)
        {
            Random random = new Random();
            Console.WriteLine(random.Next());
            Console.WriteLine(random.Next(10, 100));
        }
    }
}
```





## 1. 2. List 클래스

### 1.2.1. 생성


```c#
List<타입> 변수명 = new List<타입>();
List<타입> 변수명 = new List<타입>() { 요소1, 요소2, ... };
```

```c#
using System;
using System.Collections.Generic;

namespace ConsoleApp1
{
    class Program
    {
        static void Main(string[] args)
        {
            List<int> list = new List<int>();
            List<int> list2 = new List<int>() { 1, 2, 3, 4 };
			
            foreach (var item in list)
            {
                Console.WriteLine("Count: {0} \titem: {1}", list2.Count, item);
            }    
        }
    }
}
```

```
Count: 4	item: 1
Count: 4	item: 2
Count: 4	item: 3
Count: 4	item: 4
```



### 1.2.2. 메서드

> - 요소 추가
>   - `Add(요소)` : 요소를 추가. 요소와 타입이 맞아야 함.
> - 요소 제거
>   - `Remove(요소)` : 요소를 삭제.

#### 요소 추가

>`Add(요소)` : 요소를 추가. 요소와 타입이 맞아야 함.

```c#
using System;
using System.Collections.Generic;

namespace ConsoleApp1
{
    class Program
    {
        static void Main(string[] args)
        {
            List<int> list = new List<int>();
			
            list.Add(11);
            list.Add(12);
            list.Add(13);
            list.Add(14);
            
            foreach (var item in list) {
                Console.WriteLine("item: {0}", item);
            }
        }
    }
}
```

```
item: 11
item: 12
item: 13
item: 14
```

#### 요소 제거

> `Remove(요소)` : 요소를 삭제.

```c#
using System;
using System.Collections.Generic;

namespace ConsoleApp1
{
    class Program
    {
        static void Main(string[] args)
        {
            List<int> list = new List<int>() { 11, 12, 13, 14 };

            list.Remove(13);

            foreach (var item in list)
            {
                Console.WriteLine("item: {0}", item);
            }
        }
    }
}
```

```
item: 11
item: 12
item: 14
```



## 1.3. Math 클래스

### 1.3.1. 메서드

>`Abs(숫자)` : 절대 값을 구함.
>
>`Ceiling(숫자)` : 지정된 숫자보다 크거나 같은 최소 정수를 구함.
>
>`Floor(숫자)` : 지정된 숫자보다 작거나 같은 최대 정수를 구함.
>
>`Max(숫자, 숫자)` : 두 개의 매개변수 중에서 큰 값을 구함.
>
>`Min(숫자, 숫자)` : 두 개의 매개변수 중에 작은 값을 구함.
>
>`Round(숫자)` : 반올림함.
>
>이 외에도 많은 메서드가 있다.

```c#
using System;
using System.Collections.Generic;

namespace ConsoleApp1
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine(Math.Abs(-52273));
            Console.WriteLine(Math.Ceiling(52.273));
            Console.WriteLine(Math.Floor(52.273));
            Console.WriteLine(Math.Max(52, 273));
            Console.WriteLine(Math.Min(52, 273));
            Console.WriteLine(Math.Round(52.273));
        }
    }
}
```

```
52273
53
52
273
52
52
```







-하나의 파일에 여러 개 클래스 생성
-클래스 내부에 클래스 생성

-서로 다른 파일에 클래스 생성

-----------------------------

클래스의 변수
-인스턴스 변수
-클래스 변수
--static

# 추상화

-----------------------------

# 윈도우 폼

----------------------------------------------------------

# 메서드 형태

-----------------------------

# 매개변수 반환

-----------------------------

# 클래스 메서드

-----------------------------

# 오버로딩

-----------------------------

접근 제한자
-private
-public

-----------------------------

생성자
-private 생성자

-정적 생성자

-----------------------------

소멸자
-생성

-사용

-----------------------------

속성
-캡슐화

-겟터, 셋터

-----------------------------

윈도우폼
-이벤트 정적 연결
-이벤트 동적 연결
-이벤트 메서드의 매개변수
--sender 객체

--이벤트 정보 객체

-----------------------------

백그라운드 요소의 이벤트

----------------------------------------------------------

상속

-----------------------------

다형성

-----------------------------

is키워드

-----------------------------

클래스 자료형 변환
-일반적인 자료형 변환

-as 키워드

-----------------------------

상속의 생성자

-----------------------------

섀도잉, 하이딩

-----------------------------

하이딩과 오버라이딩
-new 메서드

-virtual, override 메서드

-----------------------------

상속과 오버라이딩 제한
-sealed 메서드
--상속 제한
--메서드 오버라이딩 제한
-abstract 키워드
--상속 제한

--메서드 오버라이딩 제한

-----------------------------

윈도우 폼
-상속, 다형성
-메시지 상자
--모달리스 메시지 상자

--모달 대화 상자

----------------------------------------------------------

제네릭

-----------------------------

out 키워드 (int.tryParse() 메서드)

-----------------------------

구조체
-생성자

-복사

-----------------------------

윈도우 폼

-상태 표시줄

-----------------------------

-----------------------------

-----------------------------

-----------------------------

-----------------------------

# 각주

[^int]: 반환값은 int 형
[^double]: 반환값은 double 형
