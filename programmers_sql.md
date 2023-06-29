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


## 모든 레코드 조회하기

- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/59034

```sql
SELECT *
FROM ANIMAL_INS
ORDER BY ANIMAL_ID ASC;
```


## 이름이 있는 동물의 아이디

- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/59407

```sql
SELECT 
    ANIMAL_ID
FROM ANIMAL_INS
WHERE NAME IS NOT NULL
ORDER BY ANIMAL_ID ASC;
```


## 역순 정렬하기

- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/59035

```sql
SELECT 
    NAME,
    DATETIME
FROM ANIMAL_INS
ORDER BY ANIMAL_ID DESC;
```


## 루시와 엘라 찾기

- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/59046

```sql
SELECT 
    ANIMAL_ID,
    NAME,
    SEX_UPON_INTAKE
FROM ANIMAL_INS
WHERE NAME IN ('Lucy', 'Ella', 'Pickle', 'Rogan', 'Sabrina', 'Mitty');
```


## 나이 정보가 없는 회원 수 구하기

- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/131528

```sql
SELECT
    COUNT(GENDER) AS USERS
FROM USER_INFO
WHERE ISNULL(AGE);
```
