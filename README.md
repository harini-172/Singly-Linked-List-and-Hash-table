# Singly-Linked-List-and-Hash-table
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class SinglyLinkedList:
    def __init__(self):
        self.head = None

    def append(self, data):
        new = Node(data)
        if not self.head:
            self.head = new
            return

        temp = self.head
        while temp.next:
            temp = temp.next
        temp.next = new

    def display(self):
        temp = self.head
        while temp:
            print(temp.data, end=" -> ")
            temp = temp.next
        print("None")

    def search(self, key):
        temp = self.head
        while temp:
            if temp.data == key:
                return True
            temp = temp.next
        return False

# Example Usage
sll = SinglyLinkedList()
sll.append(1)
sll.append(2)
sll.append(3)

sll.display()
print("Is 2 in the list?", sll.search(2))
print("Is 99 in the list?", sll.search(99))

output
1 -> 2 -> 3 -> None
Is 2 in the list? True
Is 99 in the list? False
