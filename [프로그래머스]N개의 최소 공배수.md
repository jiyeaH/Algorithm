# 프로그래머스  

## 1. 문제 정보

- 출처 : N개의 최소 공배수

- 난이도 : Level 2

## 2. 문제 해결

- 코드1 
```python

# 1.최대공약수구하기
def cal1(a,b):
	while b != 0:
		temp = b
		b = a % b
		a = temp
	return a

# 2.최소공배수구하기
def cal2(a, b):
    if a <= 0 and b <= 0:
        return -1
    return a * b // cal1(a,b)

def solution(arr):
    answer = 0
    a = arr[0]
    for i in range(len(arr)):
		a = cal2(a, arr[i])

    answer = a
    return answer
```   
