## 2-4. SELECT 연습 문제 

### NULL 
- 0이랑 다르고, ""과도 다름 => 값이 없는 상태
- NULL은 값이 없는 상태이므로, 다른 값과 직접 비교할 수 없음
                 => type2 = NULL (X)
                    type2 IS NULL (O)
- NULL이 아닌 경우:  type2 IS NOT NULL (O)

### WHERE 조건절
WHERE 절에서 여러 조건을 연결하고 싶은 경우 => AND 조건을 사용
=> WHERE
    type2 IS NULL
    AND type1 IS NOT NULL

<img width="687" alt="image" src="https://github.com/user-attachments/assets/b3e8de52-4432-4c90-829f-6ba8f4e173ca">
