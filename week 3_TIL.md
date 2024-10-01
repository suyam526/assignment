## 2-4. SELECT 연습 문제 

### NULL 
- 0이랑 다르고, ""과도 다름 => 값이 없는 상태
- NULL은 값이 없는 상태이므로, 다른 값과 직접 비교할 수 없음
                 => type2 = NULL (X)
                    type2 IS NULL (O)
- NULL이 아닌 경우:  type2 IS NOT NULL (O)
