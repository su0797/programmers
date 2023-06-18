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
