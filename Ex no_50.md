# EX 50 C function to delete a node from a Doubly Linked List at the beginning of the list.
## DATE:
## AIM:
To write a C function to delete a node from a Doubly Linked List at the beginning of the list.

## Algorithm
```
Start.
Define a variables.
Write a function to search an element in the double linked list..
Read the value using scanf.
Ask the user to make an input.
Print out the answer.
End
```

## Program:
```
/*
C function to delete a node from a Doubly Linked List at the beginning of the list.

Developed by: KAMALI.S
RegisterNumber:  212222060109

#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node* prev;
    struct Node* next;
};

struct Node* deleteAtBeginning(struct Node* head)
{
    if(head == NULL)
    {
        printf("List is already empty\n");
        return NULL;
    }

    struct Node* temp = head;
    head = head->next;

    if(head != NULL)
        head->prev = NULL;

    printf("Deleted node with value %d\n", temp->data);
    free(temp);
    return head;
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
    head = insertAtEnd(head, 30);

    display(head);

    head = deleteAtBeginning(head);

    display(head);

    return 0;
}

```

## Output:

<img width="553" height="270" alt="image" src="https://github.com/user-attachments/assets/041dbae7-8f02-4726-8a3a-f2fec0b2b5c0" />


## Result:
Thus the program was executed and the output was verified successfully.
