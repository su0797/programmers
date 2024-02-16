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
