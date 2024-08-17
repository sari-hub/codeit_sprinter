# Linked list
링크드 리스트의 개념파악 
링크드 리스트 데이터구조 파악 
	![[Pasted image 20240817151334.png]]

리스트와 링크드 리스트의 차이점  
- **메모리 구조**: 리스트는 연속적, 링크드 리스트는 비연속적
- **크기 조정**: 리스트는 고정, 링크드 리스트는 동적
- **접근성**: 리스트는 빠른 접근, 링크드 리스트는 느린 접근

링크드 리스트의 대력적 흐름파악을 하였다. 이론은 이해가 가지만 코딩해석이 아직 부족한모습이 있어 추가공부가 필수적일것이라 생각하고, 중요한 부분이라 확실히 짚고 넘어가야만 될거같다.

참고 영상 https://discord.com/channels/1262632229482528869/1268855171828678657/1274247162540068935

실습코딩
```
class Node:
    def __init__(self, data=None) -> None:
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self) -> None:
        init = Node('init')
        self.head = init
        self.tail = init
        
        self.current = None
        self.length = 0
        
    def append(self, data) -> None:
        new_node = Node(data)
        self.tail.next = new_node
        self.tail = new_node
        self.length += 1
        
    def __len__(self) -> int:
        return self.length
        
if __name__ == "__main__":
    l = LinkedList()
    l.append(10)
    l.append(20)
    l.append(30)
    l.append(40)
    l.append(50)
    l.append(15)

    l.head.data
    l.head.next.data
    l.head.next.next.data
```

