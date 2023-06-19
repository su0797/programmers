# 프로그래머스 Lv0 코딩테스트 문제풀이

## 저주의 숫자 3

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120871

```python
def solution(n):
    count10 = 0
    count3 = 0
    while count10 < n:
        count10 += 1
        count3 += 1
        while count3 % 3 == 0 or '3' in str(count3):
            count3 += 1
    return count3
```


## 대소문자 바꿔서 출력하기

- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181949

```python
s = ''
str = input()
for i in str:
    if i.islower():
        s += i.upper()
    else:
        s += i.lower()

print(s)
```


## 덧셈식 출력하기

- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181947

```python
a, b = map(int, input().strip().split(' '))
c = a + b
print(f'{a} + {b} = {c}')
```


## 문자열 붙여서 출력하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181946

```python
# 다시 푼 방법
print(input().strip().replace(' ',''))

# 처음 푼 방법
str1, str2 = input().strip().split(' ')
str3 = list(map(str, (str1, str2)))
print(''.join(str3))
```


## 문자열 돌리기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181945

```python
str = input()
a = list(str)

for i in a :
    print(i)
```


## 홀짝 구분하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181944

```python
n = int(input())
if n % 2 == 0:
    print(f'{n} is even')
else:
    print(f'{n} is odd')
```


## 문자열 겹쳐쓰기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181943

```python
# 슬라이싱을 바로 사용하기
def solution(my_string, overwrite_string, s):
    answer = my_string[:s] + overwrite_string + my_string[s + len(overwrite_string):]
    return answer
```


## 문자 리스트를 문자열로 변환하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181941

```python
def solution(arr):
    answer = ''.join(arr)
    return answer
```


## 더 크게 합치기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181939

```python
# 내가 푼 코드
def solution(a, b):
    str1 = str(a) + str(b)
    str2 = str(b) + str(a)
    if int(str1) > int( str2) or int(str1) == int(str2):
        answer = int(str1)
    elif int(str1) < int(str2):
        answer = int(str2)
    return answer

# 짧게 정리한 코드
def solution(a, b):
    return int(max(f"{a}{b}", f"{b}{a}"))
```


## 두 수의 연산값 비교하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181938

```python
def solution(a, b):
    answer = max(int((str(a) + str(b))), 2 * a * b)
    return answer
```


## n 번째 원소까지
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181889

```python
def solution(num_list, n):
    answer = num_list[:n]
    return answer

# 더 짧게 정리
def solution(num_list, n):
    return num_list[:n]
```


## n개 간격의 원소들
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181888

```python
def solution(num_list, n):
    answer = num_list[::n]
    return answer

def solution(num_list, n):
    return num_list[::n]
```
