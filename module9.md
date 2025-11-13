## EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

## Aim:
To write a C program to display stack elements using an array.
## Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
## Program:
```
#include <stdio.h>   
#include <stdlib.h>

#define SIZE 5
int stack[SIZE];
int top = -1;


void push(int value) {
    if (top == SIZE - 1) {
        printf("Stack Overflow! Cannot push %d\n", value);
    } else {
        top++;
        stack[top] = value;
        printf("%d pushed to stack.\n", value);
    }
}

void pop() {
    if (top == -1) {
        printf("Stack Underflow! No elements to pop.\n");
    } else {
        printf("%d popped from stack.\n", stack[top]);
        top--;
    }
}

void display() {
    if (top == -1) {
        printf("Stack is empty.\n");
    } else {
        printf("Stack elements are:\n");
        for (int i = top; i >= 0; i--) {
            printf("%d\n", stack[i]);
        }
    }
}

int main() {
    int choice, value;

    while (1) {
        printf("\n--- Stack Menu ---\n");
        printf("1. Push\n");
        printf("2. Pop\n");
        printf("3. Display\n");
        printf("4. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("Enter value to push: ");
                scanf("%d", &value);
                push(value);
                break;
            case 2:
                pop();
                break;
            case 3:
                display();
                break;
            case 4:
                printf("Exiting program.\n");
                exit(0);
            default:
                printf("Invalid choice! Try again.\n");
        }
    }

    return 0;
}
```

## Output:
<img width="814" height="546" alt="image" src="https://github.com/user-attachments/assets/c444ec97-124b-4937-aa41-21ff06a3159f" />


## Result:
Thus, the program to display stack elements using an array is verified successfully.
 

## EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
## Aim:
To create a C program to push the given element in to a stack using array.
##  Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
##  Program:
```
#include <stdio.h>

#define SIZE 5
float stack[SIZE];
int top = -1;

void push(float value) {
    if (top == SIZE - 1) {
        printf("Stack Overflow! Cannot push %.2f\n", value);
    } else {
        top++;
        stack[top] = value;
        printf("%.2f pushed into the stack.\n", value);
    }
}

int main() {
    float num;
    int n, i;

    printf("Enter how many elements to push (max %d): ", SIZE);
    scanf("%d", &n);

    if (n > SIZE) {
        printf("You can push only up to %d elements.\n", SIZE);
        return 0;
    }

    for (i = 0; i < n; i++) {
        printf("Enter element %d: ", i + 1);
        scanf("%f", &num);
        push(num);
    }

    printf("\nStack elements are:\n");
    for (i = top; i >= 0; i--) {
        printf("%.2f\n", stack[i]);
    }

    return 0;
}

```

##  Output:
<img width="659" height="473" alt="image" src="https://github.com/user-attachments/assets/27ca9429-2e5f-4220-ad01-11897ff065aa" />





 ## Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
## EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
## Aim:
To write a C program to display queue elements using array

## Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
## Program:

```
#include <stdio.h>
#include <stdlib.h>

#define SIZE 5

int queue[SIZE];
int front = -1;
int rear = -1;

void enqueue(int value) {
    if (rear == SIZE - 1) {
        printf("Queue Overflow! Cannot insert %d\n", value);
    } else {
        if (front == -1)
            front = 0;
        rear++;
        queue[rear] = value;
        printf("%d inserted into the queue.\n", value);
    }
}

void dequeue() {
    if (front == -1 || front > rear) {
        printf("Queue Underflow! No elements to delete.\n");
    } else {
        printf("%d deleted from the queue.\n", queue[front]);
        front++;
    }
}

void display() {
    if (front == -1 || front > rear) {
        printf("Queue is empty.\n");
    } else {
        printf("Queue elements are:\n");
        for (int i = front; i <= rear; i++) {
            printf("%d ", queue[i]);
        }
        printf("\n");
    }
}

int main() {
    int choice, value;

    while (1) {
        printf("\n--- Queue Menu ---\n");
        printf("1. Enqueue (Insert)\n");
        printf("2. Dequeue (Delete)\n");
        printf("3. Display\n");
        printf("4. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                printf("Enter value to enqueue: ");
                scanf("%d", &value);
                enqueue(value);
                break;
            case 2:
                dequeue();
                break;
            case 3:
                display();
                break;
            case 4:
                printf("Exiting program.\n");
                exit(0);
            default:
                printf("Invalid choice! Try again.\n");
        }
    }

    return 0;
}

```

## Output:
<img width="657" height="757" alt="image" src="https://github.com/user-attachments/assets/b8b4b5a0-95a9-4fe1-bfad-6775818d4536" />



## Result:
Thus, the program to display queue elements using array is verified successfully.


 
## EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
## Aim:
To write a C program to insert elements in queue using array.

## Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

## Program:
```
#include <stdio.h>

#define SIZE 5

float queue[SIZE];
int front = -1, rear = -1;

void enqueue(float value) {
    if (rear == SIZE - 1) {
        printf("Queue is full! Cannot insert %.2f\n", value);
    } else {
        if (front == -1)
            front = 0;  
        rear++;
        queue[rear] = value;
        printf("%.2f inserted into the queue.\n", value);
    }
}

void display() {
    if (front == -1) {
        printf("Queue is empty!\n");
    } else {
        printf("\nCurrent Queue Elements:\n");
        for (int i = front; i <= rear; i++) {
            printf("%.2f ", queue[i]);
        }
        printf("\n");
    }
}

int main() {
    enqueue(10.5);
    enqueue(20.3);
    enqueue(30.7);
    enqueue(40.2);
    enqueue(50.8);

    display();

    enqueue(60.1);

    display();

    return 0;
}
```

## Output:
<img width="491" height="479" alt="image" src="https://github.com/user-attachments/assets/e3325cb3-a65e-4581-93d3-33e773be0a63" />

## Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
## EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY
## Aim:

To create a function in C that deletes an element from a queue implemented using an array.

## Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



## Program:
```
#include <stdio.h>

#define SIZE 5  

float queue[SIZE];
int front = -1, rear = -1;

void enqueue(float value) {
    if (rear == SIZE - 1) {
        printf("Queue is full! Cannot insert %.2f\n", value);
    } else {
        if (front == -1)
            front = 0;  
        rear++;
        queue[rear] = value;
        printf("%.2f inserted into the queue.\n", value);
    }
}

void dequeue() {
    if (front == -1) {
        printf("Queue is empty! No elements to delete.\n");
    } else {
        printf("Deleted element: %.2f\n", queue[front]);
        front++;

        if (front > rear) {
            front = rear = -1;  // Reset queue
            printf("Queue is now empty after deletion.\n");
        }
    }
}

void display() {
    if (front == -1) {
        printf("Queue is empty!\n");
    } else {
        printf("\nCurrent Queue Elements:\n");
        for (int i = front; i <= rear; i++) {
            printf("%.2f ", queue[i]);
        }
        printf("\n");
    }
}

int main() {
    enqueue(10.5);
    enqueue(20.3);
    enqueue(30.7);
    display();

    dequeue();
    display();

    dequeue();
    dequeue();
    dequeue(); 

    return 0;
}

```

## Output:

<img width="559" height="548" alt="image" src="https://github.com/user-attachments/assets/a5bb9e1a-d98a-4c43-b975-9c5d2dbaab39" />

## Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
