# 0x1B. C - Sorting algorithms & Big O
## Resources
### Read or watch:
* [Sorting algorithm](https://en.m.wikipedia.org/wiki/Sorting_algorithm)
* [Big O notation](https://www.stackoverflow.com/questions/487258/what-is-a-plain-english-explanation-of-big-o-notation/)
* [Sorting algorithms animations](https://www.toptal.com/developers/sorting-algorithms)
* [15 sorting algorithms in 6 minutes](https://m.youtube.com/watch?v=kPRA0W1kECg&t=29s) (**WARNING**: _The following video can trigger seizure/epilepsy. It is not required for the project, as it is only a funny visualization of different sorting algorithms_)
* [Select sort](https://m.youtube.com/watch?v=Ns4TPTC8whw&t=4s)
* [Insert sort](https://m.youtube.com/watch?v=ROalU379l3U&t=9s)
* [Bubble sort](https://m.youtube.com/watch?v=lyZQPjUT5B4)
## General
* Knowledge of at least four different sorting algorithms
* What is the Big O notation, and how to evaluate the time complexity of an algorithm
* How to select the best sorting algorithm for a given input
* What is a stable sorting algorithm
## Data Structure and Functions
* For this project, the following `print_array` and `print_list` functions are being used:
```
#include <stdlib.h>
#include <stdio.h>

/**
 * print_array - Prints an array of integers
 *
 * @array: The array to be printed
 * @size: Number of elements in @array
 */
void print_array(const int *array, size_t size)
{
    size_t i;

    i = 0;
    while (array && i < size)
    {
        if (i > 0)
            printf(", ");
        printf("%d", array[i]);
        ++i;
    }
    printf("\n");
}
```
```
#include <stdio.h>
#include "sort.h"

/**
 * print_list - Prints a list of integers
 *
 * @list: The list to be printed
 */
void print_list(const listint_t *list)
{
    int i;

    i = 0;
    while (list)
    {
        if (i > 0)
            printf(", ");
        printf("%d", list->n);
        ++i;
        list = list->next;
    }
    printf("\n");
}
```
* Data structure used for doubly linked list:
```
/**
 * struct listint_s - Doubly linked list node
 *
 * @n: Integer stored in the node
 * @prev: Pointer to the previous element of the list
 * @next: Pointer to the next element of the list
 */
typedef struct listint_s
{
    const int n;
    struct listint_s *prev;
    struct listint_s *next;
} listint_t;
```
## Tests
For testing sorting algorithms with big sets of random integers: [Random.org](https://www.random.org/integer-sets/)
