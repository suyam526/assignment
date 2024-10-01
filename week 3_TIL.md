## 2-6. 연습 문제 

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


## 2-7. 연습문제
### WHERE와 HAVING
- WHERE : 원본 데이터 FROM절에 있는 데이터에 조건을 설정하고 싶은 경우
- HAVING : GROUP BY와 함께 집계 결과에 조건을 설정하고 싶은 경우 (집계 후)
-> 집계 후 조건절인데 HAVING 쓰기 싫다? -> 서브쿼리 사용 가능 (BUT 길이가 길어지므로 웬만하면 HAVING절 쓰자)
<img width="895" alt="image" src="https://github.com/user-attachments/assets/e93f16b3-81a9-4137-b937-f27a7a27e3f8">
<img width="271" alt="image" src="https://github.com/user-attachments/assets/53f6c44b-a244-4bb4-b829-4a18f0fd48f9">
<br/>

<img width="752" alt="image" src="https://github.com/user-attachments/assets/3c422e03-4e26-4f0f-a73b-37b7bde4061a">


## 2-8. 연습문제
<img width="757" alt="image" src="https://github.com/user-attachments/assets/b5fea5ae-f6e6-4b43-b5e3-01812828fe1a">
<img width="235" alt="image" src="https://github.com/user-attachments/assets/9611872f-5af0-4790-81dc-3c4162d30c80">

<img width="750" alt="image" src="https://github.com/user-attachments/assets/1388828b-71c4-4699-9b7a-a6519c10b0af">

<img width="753" alt="image" src="https://github.com/user-attachments/assets/dad8d58a-a9c0-4db6-bd11-1bac6fbc021d">

