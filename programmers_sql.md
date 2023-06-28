# 프로그래머스 SQL 코딩테스트 문제풀이

## 강원도에 위치한 생산공장 목록 출력하기

-   링크 : https://school.programmers.co.kr/learn/courses/30/lessons/131112

```sql
SELECT 
    FACTORY_ID,
    FACTORY_NAME,
    ADDRESS
FROM FOOD_FACTORY
WHERE ADDRESS LIKE '%강원도%'
ORDER BY FACTORY_ID ASC;
```

