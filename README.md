# python 스터디
## 2022-05-29


```python
s = "python syntax hilighting"
print s
```
|값|의미|기본값|
|---|:---:|---:|
| `static` | 유형(기준) 없음/ 배치불가능 | `static`|
| `relative`| 요소 자신을 기준으로 배치| |
| `absolute` | 위치 상 부모(조상)요소를 기준으로 배치 | |
| `fixed` | 브라우저 창을 기준으로 배치 | |


인용문(blockQuote)

>남의 말이나 글에서 직접 또는 간접으로 따온 문장.
>_(네이버 국어 사전)_

BREAK!

>인용문을 작성하세요!
>>중첩된 인용문(blockquote) 을 만들수 있습니다.
>>>중중첩된 인용문 1
>>>중중첩된 인용문 2
>>>중중첩된 인용문 3


'''python
| print | 형식 | 용도 |
|---|:---:|---:|
|sep| sep = ' ' | 두개 이상의 변수의 띄어쓰기 바꾸기 |

'''python
| string | start | end | step | len |
|---|:---:|:---:|:---:|---:|
|용도| 문자열 출력시, 처음 시작되는 인덱스값 | 문자열 출력시, 마지막이 되는 인덱스 값 | 띄어읽는 칸의 개수 | 문자열의 길이(글자 개수) |
|형식| [인덱스 시작값 | 끝 값 | step값] | len(string 함숫값 이름) |

'''python
|포맷팅 코드|의미|
|:---:|:---:|
|%d|정수|
|%s|문자열|
|%f|실수|
|%3d|3자리 정수|
|%5s|5자리 문자열|
|%.2f|소수점 둘쨰 짜리의 실수|



# 문자열


## 문자열 인덱싱
```python
"p  y  t  h  o  n"
[0][1][2][3][4][5]
a = "python"
a[0] = 'p'
a[3] = 'h'

a[0:5:x]
처음수 = start값
2번째 = end값
3번째 = step값
예: print(a[0:5:2])
->pto
```

## 문자열 슬라이싱
```python
 거꾸로 뒤집어 쓰기
->변수[::-1]
 뒤의 x칸만 쓰기
 ->변수[-x:]
 ```
 ## 문자열 치환
 ```python
 phone = "010-1111-2222"
 replace함수를 이용해 바꿀수 있음
 예 : 1. phone_1 = phone.replace('-',' ')
         print(phone_1)
      2.phone = phone.replace('-', ' ')
        print(phone)
 2번의 경우 원래의 변수가 replace값으로 바뀜.
```

## 문자열 다루기
```python
ex: 사이트의 뒷주소(도메인)출력
->url = "https://sharebook.kr"
split함수를 이용해 .을 기준으로 나눔
url_split = url.split('.')
print(url_split[-1]) -> 뒤로부터 1칸
```
## replace 메서드
```python
문자열은 원래 값 자체를 바꾸는것은 불가능 -> replace함수 사용
a = "python"
a_1 = a.replace('p', 'P')
print(a_1)
```



# 시퀀스 자료형



## 종류
```python
   리스트 : [x,y,z]
   튜플 : (x,y,z)
   range(x) : [0  ... x-1]
   문자열: Hello  -> [H,e,l,l,o]
```
## in 연산자
```python
a = [1,2,3,4,5,6,7]
5 in a
=>True

8 not in a 
=> False

시퀀스 객체 안에 값이 있는지 검사
모든 시퀀스 객체 사용 가능
```


## 객체 연결
```python
   시퀀스 객체1 + 시퀀스 객체2
```

## 리스트,튜플의 요소 개수 구하기
```python
   두 시퀀스 객체 모두 len(시퀀스 객체 이름)의 형식으로 사용 가능
   
ex)a = [0,10,20,30,40,50,60,70,80,90]
   len(a)
   =>10
```

## range와 문자열의 길이 구하기
```python
   range 함수
 ->range(0,10,2)
   0부터 시작 10까지 2씩 증가
   생성되는 개수 출력
   len(range(0,10,2))
   =>5
  
   문자열
 ->hello = "Hello, world!"
   len(hello)
   =>13
   공백까지 포함해 개수 검사, 문자열을 묶은 따옴표는 제외, +한글도 같은 방법
```

## 요소에 값 할당하기(교체)
```python
   리스트
 ->a = [0,0]
   a[0] = 38
   a[1] = 21
   a = [38,21]
   
  모두 같은 방법
```

## del로 요소 삭제하기
```python
   del 시퀀스 객체[인덱스]   
   
   ex)a = [38,21,53,62,19]
   del a[2]
   a = [38,21,62,19]
```

## del로 슬라이스 삭제하기
```python
   del 시퀀스객체[시작인덱스:끝인덱스]
   
   ex)a=a[0,10,20,30,40]
   del a[0:2]
   a = [30,40]
   
   튜플, range, 문자열은 del로 슬라이스 삭제 불가
```
