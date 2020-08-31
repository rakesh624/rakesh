class Node:    
    def __init__(self,data):    
        self.data = data;    
        self.previous = None;    
        self.next = None;    
            
class DoublyLinkedList:       
    def __init__(self):    
        self.head = None;    
        self.foot = None;      
    def addNode(self, data):       
        newNode = Node(data);     
        if(self.head == None):    
            self.head = self.foot = newNode;    
            self.head.previous = None;       
            self.foot.next = None;    
        else:    
            self.foot.next = newNode;    
            newNode.previous = self.foot;     
            self.foot = newNode;    
            self.foot.next = None;    
