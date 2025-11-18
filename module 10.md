# EXP NO:16 C PROGRAM TO SEARCH A GIVEN ELEMENT IN THE GIVEN LINKED LIST

## Aim:
To write a C program to search a given element in the given linked list.

## Algorithm:
1. Define the structure for a node in a linked list.  
2. Define the search function to find a specific character in the linked list.  
3. Initialize the head of the linked list as needed.  
4. Call the search function and perform other linked list operations as needed.  

## Program:
```c
struct Node{
 char data;
 struct Node *next;
}*head;
void search(char data)
{
 struct Node *ptr=head;
 char temp=data;
 int count=1;
 int flag=0;
 while(ptr!=NULL)
 {
 if(ptr->data==temp)
 {
 printf("item %c found at location %d",ptr->data,count);
 flag=1;
 }
 count++;
 ptr=ptr->next;
 }
 if(flag==0)
 {
 printf("Item not found");
 }
}
```

## Output:
![image](https://github.com/user-attachments/assets/5e9dae8b-12e9-4eb7-9862-665e399754e1)

## Result:
Thus, the program to search a given element in the given linked list is verified successfully.



---

# EXP NO:17 PROGRAM TO INSERT A NODE IN A LINKED LIST

## Aim:
To write a C program to insert a node in a linked list.

## Algorithm:
1. Define the structure for a node in a linked list  
2. Define the insert function to insert a new node with character data at the end of the linked list  
3. Initialize the head of the linked list as needed  
4. Call the insert function and perform other linked list operations as needed  

## Program:
```c
struct Node{
 char data;
 struct Node *next;
}*head;
void insert(char data)
{
 struct Node *n=malloc(sizeof(struct Node *));
 if(n==NULL)
 {
 printf("Memory allocation failed!\n");
 }
 n->data=data;
 n->next=NULL;
 if(head == NULL)
 {
 head=n;
 }
 else
 {
 struct Node *temp=head;
 while(temp->next!=NULL)
 {
 temp=temp->next;
 }
 temp->next=n;
 }
}
```

## Output:
![image](https://github.com/user-attachments/assets/22e56ea3-661b-45e3-8ab4-e9fb36ae6e8b)

## Result:
Thus, the program to insert a node in a linked list is verified successfully.



---

# EXP NO:18 C PROGRAM TO TRAVERSE A DOUBLY LINKED LIST

## Aim:
To write a C program to traverse a doubly linked list.

## Algorithm:
1. Initialize a temporary pointer (temp) to the head of the list  
2. Use a while loop to traverse the list until the end (temp == NULL)  
3. Inside the loop, print the data of the current node  
4. Move to the next node using temp = temp->next  

## Program:
```c
struct Node
{
 struct Node *prev;
 struct Node *next;
 int data;
}*head;
void display()
{
 struct Node *ptr=head;
 while(ptr!=NULL)
 {
 printf("%d ",ptr->data);
 ptr=ptr->next;
 }

}
```

## Output:
![image](https://github.com/user-attachments/assets/1df1ab36-20d0-4771-8911-ae1bc6e23ddd)

## Result:
Thus, the program to traverse a doubly linked list is verified successfully.



---

# EXP NO:19 C PROGRAM TO INSERT AN ELEMENT IN DOUBLY LINKED LIST

## Aim:
To write a C program to insert an element in doubly linked list.

## Algorithm:
1. Create a new node (newNode) and allocate memory for it  
2. Set the data of the new node  
3. If the list is empty, set the new node as the head  
4. If the list is not empty, traverse the list to find the last node  
5. Set new node's prev pointer and update links accordingly  

## Program:
```c
struct Node
{
 struct Node *prev;
 struct Node *next;
 float data;
}*head;
void insert(float data)
{
 struct Node*n=malloc(sizeof(struct Node));
 if(n==head)
 {
 printf("Memory allocation failed!\n");
 }
 n->data=data;
 n->next=NULL;
 n->prev=NULL;
 if(head==NULL)
 {
 head=n;
 }
 else
 {
 struct Node *temp=head;
 while(temp->next!=NULL)
 {
 temp=temp->next;
 }
 temp->next=n;
 n->prev=NULL;
 }
}
```

## Output:
![image](https://github.com/user-attachments/assets/66344610-d130-49e3-a161-48443016b5d3)

## Result:
Thus, the program to insert an element in doubly linked list is verified successfully.



---

# EXP NO:20 C FUNCTION TO DELETE A GIVEN ELEMENT IN THE GIVEN LINKED LIST

## Aim:
To write a C function that deletes a given element from a linked list.

## Algorithm:
1. Check if the linked list is empty  
2. Traverse the list to find the element  
3. Handle deletion of first node  
4. Handle deletion from middle or end  
5. If element not found, print a message  
6. End the function  

## Program:
```c
struct Node
{
 struct Node *prev;
 struct Node *next;
 char data;
}*head;
void delete()
{
 if(head ==NULL)
 {
 printf("UNDERFLOW\n");
 }
 else
 {
 struct Node *ptr=head;
 head=head->next;
 free(ptr);
 ptr=NULL;
 printf("Node deleted\n");
 }

}
```

## Output:
![image](https://github.com/user-attachments/assets/112cdd0e-904b-427a-98f6-43ce31de7cce)

## Result:
Thus, the function that deletes a given element from a linked list is verified successfully.
