# 프로그래머스 Python 코딩테스트 문제풀이

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


## 부분 문자열
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181842

```python
def solution(str1, str2):
    answer = 0
    if str1 in str2 :
        answer += 1
    else :
        answer = 0
    return answer

# 한줄로 if문
def solution(str1, str2):
    return 1 if str1 in str2 else 0
```


## 카운트 다운
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181899

```python
def solution(start, end):
    answer = []
    for i in range(start, end-1, -1):
        answer.append(i)
    return answer

# 한줄로 for문
def solution(start, end):
    return [ i for i in range(start, end-1, -1)]
```


## 공배수
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181936

```python
def solution(number, n, m):
    return 1 if number % n == 0 and number % m == 0 else 0
```


## 홀짝에 따라 다른 값 반환하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181935

```python
def solution(n):
    answer = 0
    if n % 2 == 1:
        for i in range(1,n+1,2):
            answer += i
    else:
        for i in range(2,n+1,2):
            answer += i**2
    return answer
```


## 조건 문자열
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181934

```python
def solution(ineq, eq, n, m):
    answer = 0
    if (ineq, eq) == ('>', '='):
        answer = 1 if n >= m else 0
    elif (ineq, eq) == ('>', '!'):
        answer = 1 if n > m else 0
    elif (ineq, eq) == ('<', '='):
        answer = 1 if n <= m else 0
    elif (ineq, eq) == ('<', '!'):
        answer =1 if n < m else 0
    return answer
```


## flag에 따라 다른 값 반환하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181933

```python
def solution(a, b, flag):
    return a + b if flag else a -b 
```


## 코드 처리하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181932

```python
# 다시 풀어보기
```


## 이어 붙인 수
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181928

```python
def solution(num_list):
    a = '' # 짝수
    b = '' # 홀수
    answer = 0
    for i in num_list:
        if i % 2 == 0:
            a += str(i)
        else:
            b += str(i)
    answer = int(a) + int(b)
    return answer
```


## 원소들의 곱과 합
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181929

```python
def solution(num_list):
    x = 1
    y = 0
    answer = 0
    for i in num_list:
        x *= i
        y += i
    answer = 0 if x > y**2 else 1 
    return answer
```


## 주사위 게임 2
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181930

```python
def solution(a, b, c):
    answer = 0
    if a == b and a == c:
        answer = (a + b + c) * (a**2 + b**2 + c**2) * (a**3 + b**3 + c**3)
    elif a == b or b == c or a == c:
        answer = (a + b + c) * (a**2 + b**2 + c**2)
    else:
        answer = a + b + c
    return answer
```


## 마지막 두 원소 (두 수가 같은 경우도 생각하기)
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181927
```python
def solution(num_list):
    if num_list[-1] > num_list[-2]:
        a = num_list[-1] - num_list[-2]
        num_list.append(a)
    elif  num_list[-1] < num_list[-2] or num_list[-1] == num_list[-2]:
        a = num_list[-1]*2
        num_list.append(a)
    return num_list
```


## 수 조작하기 1
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181926
```python
str_list = { "w" : 1, "s" : -1, "d" : 10, "a" : -10 }

def solution(n, control):
    for i in control:
        n += str_list[i]
    return n
```


## 수 조작하기 2
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181925
```python
def solution(numLog):
    answer = ''
    dic = { 1: "w", -1: "s", 10: "d", -10: "a" }
    
    for i, val in enumerate(numLog):
        if i != len(numLog)-1: 
            answer += dic[numLog[i+1] - numLog[i]]
    
    return answer
```


## 배열 두배 만들기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120809
```python
def solution(numbers):
    answer = []
    for n in numbers:
        a = n * 2
        answer.append(a)
    return answer
```


## 중앙값 구하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120811
```python
def solution(array):
    answer = 0
    array.sort()
    return array[len(array) // 2]
```


## 최빈값 구하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120812
```python
from collections import Counter

def solution(array):
    answer = Counter(array)
    if len(answer) == 1:
        return list(answer.keys())[0]
    
    common = answer.most_common(2)
    if common[0][1] == common[1][1]:
        return -1
    else:
        return common[0][0]
```


## 등차수열의 특정한 항만 더하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181931
```python
def solution(a, d, included):
    n = len(included)  
    result = 0 

    for i in range(n):
        if included[i]:  
            result += a + (i * d)  

    return result
```
또는 
```python
def solution(a, d, included):
    return sum((a + i * d) for i, is_included in enumerate(included) if is_included)
```


## 수열과 구간 쿼리 3
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181924
```python
```


## 짝수는 싫어요
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120813
```python
def solution(n):
    answer = []
    for i in range(1, n + 1, 2):
        answer.append(i)
    return answer
```


## 수열과 구간 쿼리 3
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181924
```python
def solution(arr, queries):
    for query in queries:
        i, j = query
        arr[i], arr[j] = arr[j], arr[i]

    return arr
```


## 수열과 쿠간 쿼리 2
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181923
```python
def solution(arr, queries):
    answer = []
    
    for query in queries:
        s, e, k = query
        sub_arr = arr[s:e+1] 
        filtered_values = [value for value in sub_arr if value > k]
        
        if filtered_values: 
            answer.append(min(filtered_values))
        else:
            answer.append(-1)

    return answer
```


## 수열과 구간 쿼리 4
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181922
```python
def solution(arr, queries):
    answer = []
    
    for query in queries:
        s, e, k = query
        for i in range(s, e + 1):
            if i % k == 0:
                arr[i] += 1
    
    return arr
```


## 배열 만들기 2
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181921
```python
def solution(l, r):
    answer = []

    for num in range(l, r + 1):
        if set(str(num)) <= {'0', '5'}:
            answer.append(num)

    return answer if answer else [-1]
```


## 카운트 업
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181920
```python
def solution(start_num, end_num):
    answer = list(range(start_num, end_num + 1))
    return answer
```


## 콜라츠 수열 만들기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181919
```python
def solution(n):
    answer = [n]
    
    while n != 1:
        if n % 2 == 0:
            n //= 2
        else:
            n = 3 * n + 1
        answer.append(n)

    return answer
```
