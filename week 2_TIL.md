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


# 3. 데이터 탐색 : 요약(집계,그룹화)
