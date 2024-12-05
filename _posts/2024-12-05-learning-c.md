# Day of Learning C: Building Your Knowledge Base

Welcome back, fellow learners! Continuing our dive into the world of C programming, we’ll explore more fundamental concepts and take our skills to the next level. Today, we’ll cover control structures, working with functions, and managing memory—three pillars of efficient programming in C.

## Control Structures: Decision Making and Loops

Control structures are essential for directing the flow of a program. Let’s start with an `if-else` statement:

```c
#include <stdio.h>

int main() {
    int number;
    printf("Enter a number: ");
    scanf("%d", &number);

    if (number % 2 == 0) {
        printf("%d is even.\\n", number);
    } else {
        printf("%d is odd.\\n", number);
    }

    return 0;
}
```

### Loops: Repeating Tasks Efficiently

Loops allow us to execute a block of code multiple times. Here’s a simple example using a `for` loop to print numbers from 1 to 5:

```c
#include <stdio.h>

int main() {
    for (int i = 1; i <= 5; i++) {
        printf("%d\\n", i);
    }

    return 0;
}
```

To repeat tasks until a condition is met, use a `while` loop:

```c
#include <stdio.h>

int main() {
    int counter = 0;

    while (counter < 5) {
        printf("Counter is %d\\n", counter);
        counter++;
    }

    return 0;
}
```

## Functions: Modularizing Code

Functions help you break your code into smaller, reusable parts. Let’s define a function that calculates the square of a number:

```c
#include <stdio.h>

// Function declaration
int square(int num);

int main() {
    int number;
    printf("Enter a number to find its square: ");
    scanf("%d", &number);

    printf("The square of %d is %d\\n", number, square(number));
    return 0;
}

// Function definition
int square(int num) {
    return num * num;
}
```

## Memory Management: Pointers and Dynamic Allocation

C gives you fine-grained control over memory using pointers. Here’s a basic example of pointer usage:

```c
#include <stdio.h>

int main() {
    int x = 10;
    int *ptr = &x; // Pointer to the address of x

    printf("Value of x: %d\\n", x);
    printf("Address of x: %p\\n", (void *)ptr);
    printf("Value via pointer: %d\\n", *ptr);

    return 0;
}
```

### Dynamic Memory Allocation with `malloc`

To allocate memory at runtime, use `malloc` or `calloc`:

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int n, *arr;

    printf("Enter the number of elements: ");
    scanf("%d", &n);

    // Dynamically allocate memory
    arr = (int *)malloc(n * sizeof(int));
    if (arr == NULL) {
        printf("Memory allocation failed.\\n");
        return 1;
    }

    printf("Enter %d integers:\\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    printf("You entered:\\n");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    printf("\\n");

    // Free allocated memory
    free(arr);
    return 0;
}
```

## Wrapping Up

Today, we expanded our understanding of C by exploring control structures, creating functions, and managing memory. These building blocks are critical for writing efficient and modular code. 

In the next post, we’ll dive deeper into advanced concepts like file handling, data structures, and error management. Keep experimenting with what you’ve learned, and don’t hesitate to challenge yourself with small projects.

Until next time, happy coding and keep pushing boundaries!
