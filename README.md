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
