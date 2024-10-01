## 2-6. 연습 문제 (1)

### NULL 
- 0이랑 다르고, ""과도 다름 => 값이 없는 상태
- NULL은 값이 없는 상태이므로, 다른 값과 직접 비교할 수 없음
                 => type2 = NULL (X)
                    type2 IS NULL (O)
- NULL이 아닌 경우:  type2 IS NOT NULL (O)

### WHERE 조건절
- WHERE 절에서 여러 조건을 연결하고 싶은 경우 => AND 조건을 사용
=> WHERE
    type2 IS NULL
    AND type1 IS NOT NULL

- 여러 조건 중 하나 => OR 조건을 사용 (조건문 안에 괄호 쳐야됨)
=> WHERE
    (type2 IS NULL) or (type1 = 0)

<img width="687" alt="image" src="https://github.com/user-attachments/assets/b3e8de52-4432-4c90-829f-6ba8f4e173ca">
<img width="896" alt="image" src="https://github.com/user-attachments/assets/89bf6e33-66ea-4083-8b1d-3f98fc8105b3">
<img width="894" alt="image" src="https://github.com/user-attachments/assets/3b7f331e-daa4-4003-8b8c-637e3ac741c4">

-----------

## 2-6. 연습문제 (2)
### WHERE와 HAVING
- WHERE : 원본 데이터 FROM절에 있는 데이터에 조건을 설정하고 싶은 경우
- HAVING : GROUP BY와 함께 집계 결과에 조건을 설정하고 싶은 경우 (집계 후)
-> 집계 후 조건절인데 HAVING 쓰기 싫다? -> 서브쿼리 사용 가능 (BUT 길이가 길어지므로 웬만하면 HAVING절 쓰자)
<img width="895" alt="image" src="https://github.com/user-attachments/assets/e93f16b3-81a9-4137-b937-f27a7a27e3f8">
<img width="271" alt="image" src="https://github.com/user-attachments/assets/53f6c44b-a244-4bb4-b829-4a18f0fd48f9">
<br/>

<img width="752" alt="image" src="https://github.com/user-attachments/assets/3c422e03-4e26-4f0f-a73b-37b7bde4061a">

---------

## 2-6. 연습문제 (3)
<img width="757" alt="image" src="https://github.com/user-attachments/assets/b5fea5ae-f6e6-4b43-b5e3-01812828fe1a">
<img width="235" alt="image" src="https://github.com/user-attachments/assets/9611872f-5af0-4790-81dc-3c4162d30c80">

<img width="750" alt="image" src="https://github.com/user-attachments/assets/1388828b-71c4-4699-9b7a-a6519c10b0af">

<img width="753" alt="image" src="https://github.com/user-attachments/assets/dad8d58a-a9c0-4db6-bd11-1bac6fbc021d">

--------

## 2-6. 연습문제 (4)
<img width="752" alt="image" src="https://github.com/user-attachments/assets/eadbf422-7eee-45b4-b0e1-f624c004419a">
<img width="750" alt="image" src="https://github.com/user-attachments/assets/e2d28679-34a9-40bf-8619-791e9036ce67">
<img width="750" alt="image" src="https://github.com/user-attachments/assets/f9a62d1b-ffd3-4a42-a654-12ffce49c232">

--------

## 2-6. 연습문제 (5)
<img width="752" alt="image" src="https://github.com/user-attachments/assets/a14aacc2-9d53-47bf-aaed-e640fdd409f9">
<img width="755" alt="image" src="https://github.com/user-attachments/assets/c04ac566-55f8-4354-b7c6-bfa456199d10">
<img width="751" alt="image" src="https://github.com/user-attachments/assets/c9ae9596-c4d9-4b89-a7c8-784b4be011c9">
<img width="754" alt="image" src="https://github.com/user-attachments/assets/749bb11c-82d7-435d-b2d5-24363bb9f968">
<img width="752" alt="image" src="https://github.com/user-attachments/assets/9a017eaa-d3e3-4639-bc14-9c1836a4c6e2">

------

## 2-7. 정리
<img width="540" alt="image" src="https://github.com/user-attachments/assets/6b1ac73e-34f4-4c98-a1df-00846dec0122">
-------

## 2-8. 새로운 집계 함수
* GROUP BY ALL : GROUP BY할 함수를 굳이 명시하지 않아도 이 함수를 쓰면 알아서 추측해서 실행시켜줌

-------

# 3. SQL 쿼리 잘 작성하기
## 3-1. 쿼리 작성 템플릿 & 생산성 도구
* 템플릿
  ```
  #쿼리를 작성하는 목표, 확인할 지표 : 정의
  #쿼리 계산 방법 :
  #데이터의 기간 :
  #사용할 테이블 :
  #Join Key :
  #데이터 특징 : 어떤 컬럼은 어떤 특징을 가지고 있고~

  SELECT

  FROM
  WHERE
  ```
  -> 이 템플릿을 Espanso에 넣어서 trigger 단어 입력했을 때 자동으로 생성되도록
------
## 3-2. 오류 디버깅 방법

* syntax error (문법 오류)
   -> 오류 메세지 읽고 해석
   -> 구글링/공식 문서/ChatGPT
- SELECT list must not be empty at [10:1]
- Number of arguments does not match for aggregate function COUNT (집계 함수 COUNT의 인자 수가 일치하지 않습니다)
  COUNT 함수에는 1개만 들어갈 수 있음!!!
- Syntax error : Expected end of input but got keyword SELECT (입력이 끝날 것으로 예상되었지만 SELECT 키워드가 입력되었습니다)
  SELECT 근처 확인하기, 하나의 쿼리엔 SELECT가 1개만 있어야 함!!!
  혹은 쿼리가 끝나는 부분에 ; 붙이고 실행할 부분만 드래그 앤 드랍해서 실행하기
