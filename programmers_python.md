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


## 컨트롤 제트
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120853
```python
def solution(s):
    answer = []
    for num in s.split(' '):
        try:
            answer.append(int(num))
        except:
            answer.pop()
    return sum(answer)
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


## 배열 만들기 4
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181918
```python
def solution(arr):
    stk = []
    i = 0
    
    while i < len(arr):
        if not stk or stk[-1] < arr[i]:
            stk.append(arr[i])
            i += 1
        elif stk[-1] >= arr[i]:
            stk.pop()

    return stk
```


## 간단한 논리 연산
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181917
```python
def solution(x1, x2, x3, x4):
    result = (x1 or x2) and (x3 or x4)
    return result
```


## 주사위 게임 3 (다시 풀어보기)
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181916
```python
def solution(a, b, c, d):
    nums = [a, b, c, d]
    counts = [nums.count(i) for i in nums]
    if max(counts) == 4:
        return a * 1111
    elif max(counts) == 3:
        p = nums[counts.index(3)]
        q = nums[counts.index(1)]
        return (10 * p + q) ** 2
    elif max(counts) == 2:
        if min(counts) == 2:
            return (a + c) * abs(a - c) if a == b else (a + b) * abs(a - b)
        else:
            p = nums[counts.index(2)]
            return (a * b * c * d) / p**2
    else:
        return min(nums)
```


## 글자 이어 붙여 문자열 만들기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181915
```python
def solution(my_string, index_list):
    answer = ''.join(my_string[i] for i in index_list)
    return answer
```


## 9로 나눈 나머지
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181914
```python
def solution(number):
    digit_sum = sum(int(digit) for digit in number)
    answer = digit_sum % 9
    return answer
```


## 문자열 여러 번 뒤집기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181913
```python
def solution(my_string, queries):
    for query in queries:
        start, end = query
        my_string = list(my_string)
        my_string[start:end + 1] = my_string[start:end + 1][::-1]
        my_string = ''.join(my_string)
    
    return my_string
```


## 배열 만들기 5
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181912
```python
def solution(intStrs, k, s, l):
    answer = []

    for intStr in intStrs:
        substring = intStr[s:s + l]
        num = int(substring)
        if num > k:
            answer.append(num)

    return answer
```


## 부분 문자열 이어 붙여 문자열 만들기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181911
```python
def solution(my_strings, parts):
    answer = ''
    
    for idx, val in enumerate(parts):
        answer += my_strings[idx][val[0]:val[1]+1]
    
    return answer
```


## 문자열의 뒤의 n글자
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181910
```python
def solution(my_string, n):
    answer = my_string[-n:]
    return answer
```


## 접미사 배열
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181909
```python
def solution(my_string):
    return sorted(my_string[i:] for i in range(len(my_string)))
```


## 접미사인지 확인하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181908
```python
def solution(my_string, is_suffix):
    if my_string.endswith(is_suffix):
        return 1
    else:
        return 0
```


## 문자열의 앞의 n글자
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181907
```python
def solution(my_string, n):
    answer = my_string[:n]
    return answer
```


## 접두사인지 확인하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181906
```python
def solution(my_string, is_prefix):
    if my_string.startswith(is_prefix):
        answer = 1
    else:
        answer = 0
    return answer
```


## 문자열 뒤집기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181905
```python
def solution(my_string, s, e):
    substr_to_reverse = my_string[s:e+1]
    reversed_substr = substr_to_reverse[::-1]
    answer = my_string[:s] + reversed_substr + my_string[e+1:]
    return answer
```


## 세로 읽기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181904
```python
def solution(my_string, m, c):
    result = ''
    for i in range(c-1, len(my_string), m):
        result += my_string[i]
    return result
```


## 피자 나눠먹기(1)
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120814
```python
def solution(n):
    answer = (n - 1) // 7 + 1
    return answer
```


## qr code
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181903
```python
def solution(q, r, code):
    answer = ''.join(code[i] for i in range(len(code)) if i % q == r)
    return answer
```


## 피자 나눠먹기(2)
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120815
```python
def solution(n):
    for i in range(6,606,6):
        if i%n == 0:
            answer = i/6
            break
    return answer
```


## 피자 나눠먹기(3)
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120816
```python
def solution(slice, n):
    answer=n//slice if n%slice==0 else n//slice+1
    return answer
```


## 배열의 평균값
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120817
```python
def solution(numbers):
    average = sum(numbers) / len(numbers)
    return average
```


## 옷가게 할인받기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120818
```python
def solution(price):
    discount_rate = 0  
    if price >= 500000:
        discount_rate = 0.2
    elif price >= 300000:
        discount_rate = 0.1
    elif price >= 100000:
        discount_rate = 0.05

    discounted_price = price - (price * discount_rate)

    return int(discounted_price)
```


## 아이스 아메리카노
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120819
```python
def solution(money):
    price_per_coffee = 5500  
    answer = [money // price_per_coffee , money % price_per_coffee ]
    return answer
```


## 배열 뒤집기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120821
```python
def solution(num_list):
    answer = num_list[::-1]
    return answer
```


## 짝수와 홀수
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/12937
```python
def solution(num):
    if num % 2 == 1:
        answer = 'Odd'
    else:
        answer = 'Even'
    return answer
```


## 직각삼각형 출력하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120823
```python
n = int(input())
for i in range(1,n+1):
    print('*'*i)
```


## 문자열 뒤집기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120822
```python
def solution(my_string):
    answer = my_string[::-1]
    return answer
```


## 짝수 홀수 개수
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120824
```python
def solution(num_list):
    even, odd = 0, 0
    for i in num_list:
        if i % 2 == 0:
            even += 1
        else:
            odd += 1
    answer = [even, odd]
    return answer
```


## 문자 반복 출력하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120825
```python
def solution(my_string, n):
    return ''.join(i * n for i in my_string)
```


## 특정 문자 제거하기
- 링크 https://school.programmers.co.kr/learn/courses/30/lessons/120826
```python
def solution(my_string, letter):
    return my_string.replace(letter,'')
```


## 양꼬치
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/12083
```python
def solution(n, k):
    return n*12000 + k*2000 - (n//10)*2000
```


## 짝수의 합
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120831
```python
def solution(n):
    answer = 0
    for i in range(n+1):
        if i % 2 == 0:
            answer += i
    return answer
```


## 배열 자르기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120833
```python
def solution(numbers, num1, num2):
    answer = numbers[num1:num2+1]
    return answer
```


## 외계행성의 나이
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120834
```python
def solution(age):
    answer = ''
    alpha = {'0':'a', '1':'b', '2':'c', '3':'d', '4':'e', '5':'f',
            '6':'g', '7':'h', '8':'i', '9':'j'}
    for i in str(age):
        answer+=(alpha[i])
    return answer
```


## 진로 순서 정하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120835
```python
def solution(emergency):
    answer = []
    count = 1
    for i in emergency:
        for j in emergency:
            if (i != j and i < j):
                count += 1
        answer.append(count)
        count = 1
    return answer
```


## 순서쌍의 개수
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120836
```python
def solution(n):
    answer = 0
    for i in range(1, n + 1):
        if n % i == 0:
            answer += 1
    return answer
```


## 개미 군단
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120837
```python
def solution(hp):
    return (hp // 5) + ((hp % 5) // 3) + ((hp % 5) % 3)
```


## 모스 부호(1)
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120838
```python
def solution(letter):
    answer = ''

    morse = { 
        '.-':'a','-...':'b','-.-.':'c','-..':'d','.':'e','..-.':'f',
        '--.':'g','....':'h','..':'i','.---':'j','-.-':'k','.-..':'l',
        '--':'m','-.':'n','---':'o','.--.':'p','--.-':'q','.-.':'r',
        '...':'s','-':'t','..-':'u','...-':'v','.--':'w','-..-':'x',
        '-.--':'y','--..':'z'
    }   

    letter_ls = letter.split()
    for l in letter_ls:
        answer += morse[l]

    return answer
```


## 가위 바위 보
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120839
```python
def solution(rsp):
    answer = ''
    for i in rsp:
        if i == '2':
            answer += '0'
        elif i == '0':
            answer += '5'
        elif i == '5':
            answer += '2'
    return answer
```


## 구슬을 나누는 경우의 수
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120840
```python
from math import factorial

def solution(balls, share): 
    n = factorial(balls)
    m = factorial(share)
    nm = factorial(balls - share) * m
    return n / nm
```


## 점의 위치 구하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120841
```python
def solution(dot):
    if dot[0] > 0:
        if dot[1] > 0:
            return 1
        return 4
    else:
        if dot[1] > 0:
            return 2
        return 3
```


## 2차원으로 만들기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120842
```python
def solution(num_list, n):
    answer = []
    for i in range(0, len(num_list), n):
        answer.append(num_list[i:i+n])
    return answer
```

## 공 던지기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120843
```python
def solution(numbers, k):
    return numbers[2 * (k - 1) % len(numbers)]
```


## 배열 회전시키기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120844
```python
from collections import deque

def solution(numbers, direction):
    numbers = deque(numbers)
    if direction == 'right':
        numbers.rotate(1)
    else:
        numbers.rotate(-1)
    return list(numbers)
```


## 주사위의 개수
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120845
```python
def solution(box, n):
    a = box[0] // n
    b = box[1] // n
    c = box[2] // n
    answer = a * b * c
    return answer
```


## 합성수 찾기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120846
```python
def solution(n):
    arr = []
    answer = 0
    for i in range(2, n+1):
        for j in range(1, i+1):
            if i % j == 0:
                arr.append(i)
        if arr.count(i) >= 3:
            answer += 1
    return answer
```


## 최댓값 만들기 (1)
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120847
```python
def solution(numbers):
    numbers.sort()
    return numbers[-1] * numbers[-2]
```


## 팩토리얼
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120848
```python
from math import factorial

def solution(n):
    answer = 10
    while n < factorial(answer):
        answer -= 1
    return answer
```


## 모음 제거
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120849
```python
def solution(my_string):
    vowels = ['a','e','i','o','u']
    for vowel in vowels:
        my_string = my_string.replace(vowel, '')
    return my_string
```


## 문자열 정렬하기(1)
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120850
```python
def solution(my_string):
    answer = []
    for i in my_string:
        if i.isdigit():
            answer.append(int(i))
    answer.sort()
    return answer
```


## 소인수분해
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120852
```python
def solution(n):
    answer = []
    divide = 2
    while divide <= n:
        if n % divide == 0:
            if divide not in answer:
                answer.append(divide)
            n //= divide
        else:
            divide += 1
    return answer
```


## 배열 원소의 길이
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120854
```python
def solution(strlist):
    answer = []
    for word in strlist:
        answer.append(len(word))
    return answer
```


## 중복된 문자 제거
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120888
```python
def solution(my_string):
    answer = ''
    for i in my_string:
        if i not in answer:
            answer+=i
    return answer
```


## 삼각형의 완성 조건(1)
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120889
```python
def solution(sides):
    sides.sort()
    return 1 if sides[0]+sides[1]>sides[2] else 2
```


## 가까운 수
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120890
```python
def solution(array, n):
    array.sort()
    temp = []

    for i in array :
        temp.append( abs(n-i) )

    return array[temp.index(min(temp))]
```


## 369게임
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120891
```python
def solution(order):
    answer = 0
    for i in str(order):
        if i in ["3", "6", "9"]:
            answer += 1
    return answer
```


## 암호해독
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120892
```python
def solution(cipher, code):
    return ''.join(x for i, x in enumerate(cipher, 1) if i % code == 0)
```


## 대문자와 소문자
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120893
```python
def solution(my_string):
    return my_string.swapcase()
```


## 영어가 싫어요
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120894
```python
def solution(numbers):
    nums = ["zero", "one", "two", "three", "four", "five", "six", "seven", "eight", "nine"]
    for i, num in enumerate(nums):
        numbers = numbers.replace(num,str(i))

    return int(numbers)
```


## 인덱스 바꾸기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120895
```python
def solution(my_string, num1, num2):
    my_string = list(my_string)
    my_string[num1],my_string[num2] = my_string[num2],my_string[num1]
    return ''.join(my_string)
```


## 한 번만 등장한 문자
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120896
```python
def solution(s):
    answer = ''
    for i in s:
        if s.count(i) == 1:
            answer += i
    answer = ''.join(sorted(answer))

    return answer
```


## 약수 구하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120897
```python
def solution(n):
    answer = [i for i in range(1, n+1) if n % i == 0]
    return answer
```


## 편지
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120898
```python
def solution(message):
    return len(message)*2
```


## 가장 큰 수 찾기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120899
```python
def solution(array):
    return [max(array), array.index(max(array))]
```


## 문자열 계산하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120902
```python
def solution(my_string):
    return eval(my_string)
```


## 배열의 유사도
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120903
```python
def solution(s1, s2):
    answer = 0

    for i in s1:
        for j in s2:
            if i == j:
                answer += 1

    return answer
```


## 숫자 찾기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120904
```python
def solution(num, k):
    answer = (str(num).find(str(k))+1)
    if answer == 0:
        answer = -1
    return answer
```


## n의 배수 고르기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120905
```python
def solution(n, numlist):
    answer = [i for i in numlist if i%n==0]
    return answer
```


## 자릿수 더하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120906
```python
def solution(n):
    return sum(int(i) for i in str(n))
```


## OX퀴즈
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120907
```python
def solution(quiz):
    answer = []
    for q in quiz:
        p, a = q.split("=")
        if eval(p) == int(a):
            answer.append("O")
        else:
            answer.append("X")
    return answer
```


## 문자열안에 문자열
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120908
```python
def solution(str1, str2):
    return 1 if str2 in str1 else 2
```


## 제곱수 판별하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120909
```python
def solution(n):
    return 1 if (n ** 0.5) % 1 == 0 else 2
```


## 세균 증식
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120910
```python
def solution(n, t):
    return n*(2**t)
```


## 문자열 정렬하기 (2)
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120911
```python
def solution(my_string):
    answer = ''
    for i in my_string:
        answer += i.lower()
    return ''.join(sorted(answer))
```


## 7의 개수
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120912
```python
def solution(array):
    return str(array).count('7')
```


## 잘라서 배열로 저장하기 
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120913
```python
def solution(my_str, n):
    return [my_str[i:i+n] for i in range(0, len(my_str), n)]
```


## 중복된 숫자 개수
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120583
```python
def solution(array, n):
    return array.count(n)
```


## 머쓱이보다 키 큰 사람
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120585
```python
def solution(array, height):
    answer = 0
    for i in array:
        if i > height:
            answer += 1
    return answer
```


## 직사각형 넓이 구하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120860
```python
def solution(dots):
    [[x1, y1], [x2, y2], [x3, y3], [x4, y4]] = dots
    width = max(x1,x2,x3,x4) - min(x1,x2,x3,x4)
    height = max(y1,y2,y3,y4) - min(y1,y2,y3,y4)
    return width*height
```


## 캐릭터의 좌표
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120861 (이건 다시 풀어보기...)
```python
def solution(keyinput, board):
    answer = [0, 0]
    
    x = board[0] // 2
    y = board[1] // 2
    
    for i in keyinput:
        if i == "up" and answer[1]+1 <= y:
            answer[1] += 1
        elif i == "down" and answer[1]-1 >= -y:
            answer[1] -= 1
        elif i == "left" and answer[0]-1 >= -x:
            answer[0] -= 1
        elif i == "right" and answer[0]+1 <= x:
            answer[0] += 1
    
    return answer
```


## 최댓값 만들기 (2)
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120862
```python
def solution(numbers):
    numbers = sorted(numbers)
    # numbers.sort()
    return max(numbers[0] * numbers[1], numbers[-1]*numbers[-2]) 
```


## 다항식 더하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120863 (다시 풀어보기)
```python
def solution(polynomial):
    xnum = 0
    const = 0
    for c in polynomial.split(' + '):
        if c.isdigit():
            const+=int(c)
        else:
            xnum = xnum+1 if c=='x' else xnum+int(c[:-1])
    if xnum == 0:
        return str(const)
    elif xnum==1:
        return 'x + '+str(const) if const!=0 else 'x'
    else:
        return f'{xnum}x + {const}' if const!=0 else f'{xnum}x'
```


## 숨어있는 숫자의 덧셈 (2)
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120864
```python
def solution(my_string):
    s = ''.join(i if i.isdigit() else ' ' for i in my_string)
    return sum(int(i) for i in s.split())
```


## 안전지대 
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120866
```python
def solution(board):
    n = len(board)
    danger = set()
    for i, row in enumerate(board):
        for j, x in enumerate(row):
            if not x:
                continue
            danger.update((i+di, j+dj) for di in [-1,0,1] for dj in [-1, 0, 1])
    return n*n - sum(0 <= i < n and 0 <= j < n for i, j in danger)
```


## 삼각형의 완성조건 (2)
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120868
```python
def solution(sides):
    # n이 1씩 증가하면서 가장 긴변의 길이가 n으로 바뀌는 때를 기준으로
    # 이전에는 min(sides) - 1개의 삼각형을 만들수 있고
    # 이후로는 min(sides) 개의 삼각형을 만들 수 있음
    return 2*min(sides) - 1
```


## 외계어 사전
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120869
```python
def solution(spell, dic):
    spell = set(spell)
    for s in dic:
        if not spell-set(s):
            return 1
    return 2
```


## 평행 
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120875
```python
def solution(dots):
    [[x1, y1], [x2, y2], [x3, y3], [x4, y4]]=dots
    answer1 = ((y1-y2)*(x3-x4) == (y3-y4)*(x1-x2))
    answer2 = ((y1-y3)*(x2-x4) == (y2-y4)*(x1-x3))
    answer3 = ((y1-y4)*(x2-x3) == (y2-y3)*(x1-x4))
    return 1 if answer1 or answer2 or answer3 else 0
```


## 겹치는 선분의 길이
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120876
```python
def solution(lines):
    answer = set()
    for i, a in enumerate(lines):
        for b in lines[i + 1:]:
                answer |= set(range(a[0], a[1])) & set(range(b[0], b[1]))
    return len(answer)
```


## 유한소수 판별하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120878
```python
from math import gcd
def solution(a, b):
    b //= gcd(a,b)
    while b%2==0:
        b//=2
    while b%5==0:
        b//=5
    return 1 if b==1 else 2
```


## 특이한 정렬
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120880
```python
def solution(numlist, n):
    return sorted(numlist,key = lambda x: [abs(x-n),-x])
```


## 등수 매기기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/120882
```python
def solution(score):
    a = sorted([sum(i) for i in score], reverse = True)
    return [a.index(sum(i))+1 for i in score]
```
