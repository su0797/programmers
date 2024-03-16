# 프로그래머스 Python 코딩테스트 문제풀이


## 대문자로 바꾸기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181877
  ```python
  def solution(myString):
    return myString.upper()
  ```


## 정수 찾기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181840
```python
def solution(num_list, n):
  answer = 0
  if n in num_list:
      answer = 1
  else:
      answer = 0
  return answer
```


## 배열 비교하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/181856
```python
def solution(arr1, arr2):
  if len(arr1) > len(arr2):
      return 1
  elif len(arr1) < len(arr2):
      return -1
  else:
      if sum(arr1) > sum(arr2):
          return 1
      elif sum(arr1) < sum(arr2):
          return -1
      else:
          return 0
```


## 자릿수 더하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/12931
```python
def solution(n):
    answer = 0
    for i in str(n):
        answer += int(i)
    # [실행] 버튼을 누르면 출력 값을 볼 수 있습니다.
    print('Hello Python')

    return answer
```


## 문자열을 정수로 바꾸기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/12925
```python
def solution(s):
    return int(s)
```


## 약수의 합
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/12928
```python
def solution(n):
    answer = 0
    for i in range(1, n+1):
        if n % i == 0:
            answer += i
    return answer
```


## 평균 구하기
- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/12944
```python
def solution(arr):
    answer = 0
    answer = sum(arr) / len(arr)
    return answer
```
