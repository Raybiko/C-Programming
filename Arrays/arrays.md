# ARRAYS

Method of clubbing multiple entities of similar type into a large group.
-
---

## DECLARE ARRAY:
---

define the data type (like int) and specify the name of the array followed by square brackets[].

```c
int myNumbers[];{a,b,c}
```
---

## INITIALIZING ARRAYS 
---

### ***Method 1: Initialize an array using an Initializer List***
---

>>An initializer list initializes elements of an array in the order of the list.

```c
int arr[5] = {1, 2, 3, 4, 5};

int arr[5] = {1, 2, 3, 4, 5};
```

```c
// Valid. Size of the array is taken as the number of elements
// in the initializer list (5)
int arr[5] = {1, 2, 3, 4, 5};

#include <stdio.h>

int main() {
    // You must mention the size of the array, if you want more than one
    // element initialized to 0
    // Here, all 5 elements are set to 0!
    int arr[5] = {0};
    for (int i=0; i<5; i++) {
        printf("%d\n", arr[i]);
    }
    return 0;
}
```

Output

0
0
0
0
0

>>>If you’re using multi-dimensional arrays, you can still initialize them all in one block, since arrays are stored in a row-wise manner.

```c
#include <stdio.h>

int main() {
    int arr[3][3] = {1,2,3,4,5,6,7,8,9};
    for (int i=0; i<3; i++)
        for (int j=0; j<3; j++)
            printf("%d\n", arr[i][j]);
    return 0;
}

A similar method can also be used for other datatypes, like float, char, char*, etc.

#include <stdio.h>

int main() {
    // Array of char* elements (C "strings")
    char* arr[9] = { "Hello", [1 ... 7] = "JournalDev", "Hi" };
    for (int i=0; i<9; i++)
        printf("%s\n", arr[i]);
    return 0;
}
```
**Output**

>Hello
>JournalDev
>
>JournalDev
>
>JournalDev
>
>JournalDev
>
>JournalDev
>
>JournalDev
>
>JournalDev
>
>Hi

---

### ***Method 2: Initialize an array in C using a for loop***
---

We can also use the for loop to set the elements of an array.

```c
#include <stdio.h>

int main() {
    // Declare the array
    int arr[5];
    for (int i=0; i<5; i++)
        arr[i] = i;

    for (int i=0; i<5; i++)
        printf("%d\n", arr[i]);

    return 0;
}
```

__Output__

- 0
- 1
- 2
- 3
- 4

---

### ***Method 3: Using Designated Initializers (For gcc compiler only)***
---

If you’re using _gcc_ as your __C compiler__, you can use designated initializers, to set a specific range of the ~~array~~ to the same value.

```c
#include <stdio.h>

int main() {
    int arr[9] = { 0, [1 ... 7] = 10, 0 };
    for (int i=0; i<9; i++)
        printf("%d\n", arr[i]);
    return 0;
}
```

[For more info on Arrays click link:](https://www.tutorialspoint.com/cprogramming/c_arrays.htm "C Tutorials")

[![Image]()]()
