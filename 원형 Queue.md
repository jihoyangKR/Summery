# Queue

### 원형 큐

```python
front = rear = 0
# Qsieze => Queue의 길이

def enqueue(item):
    global rear
    rear = (rear + 1) % Qsize
    Q[rear] = item

def dequeue(item):
    global front
    front = (front + 1) % Qsize
    return Q[front]

def isfull():
    return front == (rear + 1) % Qsize # rear+1 => 현재 rear 위치 다음을 check 한다.

def isempty():
    return front == rear

# X % N -> 나머지는 항상 0~N-1 값이 나온다. 이때의 나머지는 인덱스값이 된다.

```