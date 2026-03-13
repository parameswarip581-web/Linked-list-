# Linked-list-
Practice program 
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
class LinkedList:
    def __init__(self):
        self.head = None
    def insert(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
        else:
            temp = self.head
            while temp.next:
                temp = temp.next
            temp.next = new_node
        print "Inserted:", data
    def delete(self, data):
        temp = self.head
        if temp and temp.data == data:
            self.head = temp.next
            print "Deleted:", data
            return
        prev = None
while temp and temp.data != data:
            prev = temp
            temp = temp.next
        if temp is None:
            print "Element not found"
            return
        prev.next = temp.next
        print "Deleted:", data
    def display(self):
        if not self.head:
            print "List is empty"
            return
        temp = self.head
        print "List elements:",
        while temp:
            print temp.data,
            temp = temp.next
        print
ll = LinkedList()
while True:
    print "\n1. Insert  2. Delete  3. Display  4. Exit"
    choice = int(raw_input("Enter choice: "))
    if choice == 1:
        val = int(raw_input("Enter element: "))
        ll.insert(val)
    elif choice == 2:
        val = int(raw_input("Enter element to delete: "))
        ll.delete(val)
elif choice == 3:
        ll.display()
    elif choice == 4:
        print "Exit"
        break
    else:
        print "Invalid choice"
Output :
Enter choice: 1
Enter element: 10
Inserted: 10

Enter choice: 1
Enter element: 20
Inserted: 20

Enter choice: 3
List elements: 10 20
