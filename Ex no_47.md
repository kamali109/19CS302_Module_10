# EX 47 C function to insert a node in a linked list.
## DATE:
## AIM:
To write a C function to insert a node in a linked list.

## Algorithm
1. 
2. 
3. 
4.  
5.   

## Program:
```
/*
C function to insert a node in a linked list.

Developed by: KAMALI.S
RegisterNumber:  212222060109
*/
/*

#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node* next;
};

struct Node* insert(struct Node* head, int value)
{
    struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));
    newNode->data = value;
    newNode->next = NULL;

    if(head == NULL)
    {
        head = newNode;
    }
    else
    {
        struct Node* temp = head;
        while(temp->next != NULL)
        {
            temp = temp->next;
        }
        temp->next = newNode;
    }
    return head;
}

void display(struct Node* head)
{
    struct Node* current = head;
    while(current != NULL)
    {
        printf("%d -> ", current->data);
        current = current->next;
    }
    printf("NULL\n");
}

int main()
{
    struct Node* head = NULL;

    head = insert(head, 100);
    head = insert(head, 200);
    head = insert(head, 300);

    display(head);

    return 0;
}

```

## Output:

<img width="404" height="224" alt="image" src="https://github.com/user-attachments/assets/ba15be46-2b2b-47fe-b3e1-f198cc982a82" />


## Result:
Thus the program was executed and the output was verified successfully.
