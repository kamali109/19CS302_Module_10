# EX 46 C function to traverse the linked list and display it in the following format.

## AIM:
To write a C function to traverse the linked list and display it in the following format.

## Algorithm
1. 
2. 
3. 
4.  
5.   

## Program:
```
/*
C function to traverse the linked list and display it in the following format.

Developed by: KAMALI.S
RegisterNumber:  212222060109
*/
/*
C function to traverse the linked list and display it in the following format.

Developed by: Esaki Muthu E
RegisterNumber:  212222060055
*/
#include <stdio.h>
#include <stdlib.h>

struct Node
{
    int data;
    struct Node* next;
};

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
    struct Node* head = (struct Node*)malloc(sizeof(struct Node));
    struct Node* second = (struct Node*)malloc(sizeof(struct Node));
    struct Node* third = (struct Node*)malloc(sizeof(struct Node));

    head->data = 10;
    head->next = second;

    second->data = 20;
    second->next = third;

    third->data = 30;
    third->next = NULL;

    display(head);

    return 0;
}
```

## Output:

![Uploading image.png…]()


## Result:
Thus the program was executed and the output was verified successfully.
