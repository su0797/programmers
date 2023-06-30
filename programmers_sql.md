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


## 가장 비싼 상품 구하기

- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/131697

```sql
# 내가 푼 방법
SELECT 
    PRICE AS MAX_PRICE
FROM PRODUCT
ORDER BY PRICE DESC
LIMIT 1;

# 다른 방법
SELECT 
    MAX(PRICE) AS MAX_PRICE
FROM PRODUCT;
```


## 최솟값 구하기

- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/59038

```sql
SELECT 
    MIN(DATETIME) AS TIME
FROM ANIMAL_INS;
```


## 동물 수 구하기

- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/59406

```sql
SELECT
    COUNT(ANIMAL_ID)
FROM ANIMAL_INS;
```


## 중복 제거하기

- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/59408

```sql
SELECT
    COUNT(DISTINCT NAME) AS count
FROM ANIMAL_INS;
```


## 재구매가 일어난 상품과 회원 리스트 구하기

- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/131536

```sql
SELECT 
    USER_ID, 
    PRODUCT_ID
FROM ONLINE_SALE  
GROUP BY USER_ID, PRODUCT_ID
HAVING count(PRODUCT_ID) >= 2
ORDER BY USER_ID ASC, PRODUCT_ID DESC;
```


## 어린 동물 찾기

- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/59037#fn1

```sql
SELECT 
    ANIMAL_ID,
    NAME
FROM ANIMAL_INS
WHERE INTAKE_CONDITION != 'Aged'
GROUP BY ANIMAL_ID;
```


## 인기있는 아이스크림

- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/133024

```sql
SELECT FLAVOR
FROM FIRST_HALF
ORDER BY TOTAL_ORDER DESC, SHIPMENT_ID ASC;
```


## 상위 n개 레코드

- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/59405

```sql
SELECT 
    NAME
FROM ANIMAL_INS
ORDER BY DATETIME ASC
LIMIT 1;
```


## 여러 기준으로 정렬하기

- 링크 : https://school.programmers.co.kr/learn/courses/30/lessons/59404

```sql
SELECT 
    ANIMAL_ID,
    NAME,
    DATETIME
FROM ANIMAL_INS
ORDER BY NAME, DATETIME DESC;
```
