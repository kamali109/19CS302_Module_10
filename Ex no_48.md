# EX 48 C functions to perform all basic operations in Doubly Linked List.

## AIM:
To write a C functions to perform all basic operations in Doubly Linked List.

## Algorithm
1. 
2. 
3. 
4.  
5.   

## Program:
```
/*
C functions to perform all basic operations in Doubly Linked List.

Developed by: KAMALI.S
RegisterNumber:  212222060109
*/
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node* prev;
    struct Node* next;
};

struct Node* insertAtBeginning(struct Node* head, int value)
{
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = value;
    newNode->prev = NULL;
    newNode->next = head;

    if(head != NULL)
        head->prev = newNode;

    return newNode;
}

struct Node* insertAtEnd(struct Node* head, int value)
{
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = value;
    newNode->next = NULL;

    if(head == NULL)
    {
        newNode->prev = NULL;
        return newNode;
    }

    struct Node* temp = head;
    while(temp->next != NULL)
        temp = temp->next;

    temp->next = newNode;
    newNode->prev = temp;

    return head;
}

struct Node* deleteNode(struct Node* head, int value)
{
    struct Node* temp = head;

    while(temp != NULL && temp->data != value)
        temp = temp->next;

    if(temp == NULL)
    {
        printf("Node not found\n");
        return head;
    }

    if(temp->prev != NULL)
        temp->prev->next = temp->next;
    else
        head = temp->next;

    if(temp->next != NULL)
        temp->next->prev = temp->prev;

    free(temp);
    printf("Node with value %d deleted\n", value);
    return head;
}

void display(struct Node* head)
{
    struct Node* temp = head;
    printf("Doubly Linked List: ");
    while(temp != NULL)
    {
        printf("%d <-> ", temp->data);
        temp = temp->next;
    }
    printf("NULL\n");
}

int main()
{
    struct Node* head = NULL;

    head = insertAtEnd(head, 10);
    head = insertAtEnd(head, 20);
    head = insertAtBeginning(head, 5);
    head = insertAtEnd(head, 30);

    display(head);

    head = deleteNode(head, 20);
    display(head);

    return 0;
}

 
*/
```

## Output:
<img width="592" height="269" alt="image" src="https://github.com/user-attachments/assets/36a56a18-ad6e-4970-9470-47512a85def1" />



## Result:
Thus the program was executed and the output was verified successfully.
