# 1. 데이터 탐색
```
SELECT  # 테이블의 어떤 컬럼을 선택(출력)할 것인가?
  Col1 AS new_name,  #AS {컬럼 새 별칭} : {컬럼 새 별칭}으로 이름 바꿔줘
  Col2,
  Col3
FROM Dataset.Table  # 어떤 테이블에서 데이터를 확인할 것인가?
WHERE  # 만약 원하는 조건이 있다면 어떤 조건인가?
  Col1 = 1  # 조건문
```

<img width="437" alt="2" src="https://github.com/user-attachments/assets/420e9d82-c256-4bd8-b02f-bbfc47c3cbf2">

```
SELECT
*
FROM basic.pokemon
WHERE
  type1 = "Fire"

* : 모든 컬럼을 출력하겠다
```

```
생각 순서: FROM-WHERE-SELECT
작성 순서: SELECT-FROM-WHERE  (이 순서 아니면 실행 x)
```

<img width="473" alt="1" src="https://github.com/user-attachments/assets/50a76048-0ce5-4e1c-a3a4-79b782ccb11e">

# 2. 문제 풀기
```
-- 문제 1. trainer 테이블에 있는 모든 데이터를 보여주는 SQL 쿼리를 작성해주세요
-- 1) Trainer 테이블에 어떤 데이터가 있는지 확인해보자
-- 2) Trainer 테이블을 어디에 명시해야 할까? => FROM
-- 3) 필터링 조건 있을까? => 모든 데이터 불러오는 것이므로 필터링 필요 X
-- 4) 모든 데이터라는게.. => 모든 데이터 = 모든 컬럼일 수도 있겠다 (추측) 가지고 쿼리 작성 OR 애매하면 모든 데이터의 정의를 먼저 하기

SELECT  
  *
FROM `notional-impact-435714-m9.basic.trainer` 
```

```
-- 2번. trainer 테이블에 있는 트레이너의 name을 출력하는 쿼리를 작성해주세요.
-- 1) trainer 테이블 사용
-- 2) name 컬럼을 사용

SELECT
  name
FROM basic.trainer
```

```
-- 3번. trainer 테이블에 있는 트레이너의 name, age를 출력하는 쿼리를 작성해주세요

SELECT
  name,
  age
FROM basic.trainer
```

```
-- 4번. trainer의 테이블에서 id가 3인 트레이너의 name, age, hometown을 출력하는 쿼리를 작성해주세요

SELECT
  name,
  age,
  hometown
FROM basic.trainer
WHERE 
  id = 3
```

```
-- 5. pokemon 테이블에서 "피카츄"의 공격력과 체력을 확인할 수 있는 쿼리를 작성해주세요
SELECT
  attack,
  HP
FROM basic.pokemon
WHERE
  kor_name = "피카츄"
```

# 3. 데이터 탐색 : 요약(집계,그룹화)
