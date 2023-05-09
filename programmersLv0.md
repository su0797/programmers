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
