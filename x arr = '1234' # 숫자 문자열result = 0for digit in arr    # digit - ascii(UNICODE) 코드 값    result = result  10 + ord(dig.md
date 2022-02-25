```python
arr = '1234' # 숫자 문자열

result = 0

for digit in arr:
    # digit -> ascii(UNICODE) 코드 값
    result = result * 10 + ord(digit) - ord('0')
print(result)

arr = [1, 2, 3, 4]
result = 0

for digit in arr:
    result = result * 10 + digit
print(result) # => 1234
```

정수를 한자리씩 쪼개기



```python
num = 1234
while num:
    arr = [num % 10] + arr
    num = num // 10
print(arr)

#문자열로 입력받기
while num:
    n = chr(ord('0') + num % 10)
    arr = n + arr
    num = num // 10
print(arr type(arr))
# 뒤집기
arr = list['algorithm']
N = len(arr)
for i in range(N//2):
	arr[i], arr[N-1-i] = arr[N-1-i], arr[i]
```

```python
N = int(input())
arr = list(map(int, input()))
cnt=0
max_v=0
if arr[i]==0:
    cnt=0
if arr[i]==1:
    cnt+=1
    if max_v < cnt:
        max_v=cnt
print(cnt)
```

