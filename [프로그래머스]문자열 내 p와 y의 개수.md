# 프로그래머스  

## 1. 문제 정보

- 출처 : 문자열 내 p와 y의 개수

- 난이도 : Level 1

## 2. 문제 해결

- 코드1 (for문을 list의 원소에 따라 반복)

```python
def solution(s):
    answer = True
    p = 0
    y = 0
    s = list(s)
    
    for i in s:
        if i == 'p' or i == 'P':
            p = p + 1
        elif i == 'y' or i =='Y':
            y = y + 1
    
    if p != y :
        return False

    return True
```   
   
- 코드2 (for문을 인덱스에 따라 반복)

```python
def solution(s):
    answer = True
    p = 0
    y = 0
    s = list(s)
    
    for i in range(len(s)):
        if s[i] == 'p' or s[i] == 'P':
            p = p + 1
        elif s[i] == 'y' or s[i] =='Y':
            y = y + 1
    if p != y :
        return False

    return True
```
