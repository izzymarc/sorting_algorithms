In this project, various sorting algorithms were developed and implemented.

## Tests :heavy_check_mark:

* [tests](./tests): Directory containing test scripts.

## Helper Files :raised_hands:

* [print_array.c](./print_array.c): A C function for displaying an integer array.
* [print_list.c](./print_list.c): A C function for outputting a `listint_t` doubly-linked list.

## Header Files :file_folder:

* [sort.h](./sort.h): Header file with all the definitions and prototypes for the types and functions created for this project.

Data Structure:
```
typedef struct listint_s
{
    const int n;
    struct listint_s *prev;
    struct listint_s *next;
} listint_t;
```

Function Prototypes:

| File                        | Prototype                                         |
| --------------------------- | ------------------------------------------------- |
| `print_array.c`             | `void print_array(const int *array, size_t size)` |
| `print_list.c`              | `void print_list(const listint_t *list)`          |
| `0-bubble_sort.c`           | `void bubble_sort(int *array, size_t size);`      |
| `1-insertion_sort_list.c`   | `void insertion_sort_list(listint_t **list);`     |
| `2-selection_sort.c`        | `void selection_sort(int *array, size_t size);`   |
| `3-quick_sort.c`            | `void quick_sort(int *array, size_t size);`       |
| `100-shell_sort.c`          | `void shell_sort(int *array, size_t size);`       |
| `101-cocktail_sort_list.c`  | `void cocktail_sort_list(listint_t **list);`      |
| `102-counting_sort.c`       | `void counting_sort(int *array, size_t size);`    |
| `103-merge_sort.c`          | `void merge_sort(int *array, size_t size);`       |
| `104-heap_sort.c`           | `void heap_sort(int *array, size_t size);`        |
| `105-radix_sort.c`          | `void radix_sort(int *array, size_t size);`       |
| `106-bitonic_sort.c`        | `void bitonic_sort(int *array, size_t size);`     |
| `107-quick_sort_hoare.c`    | `void quick_sort_hoare(int *array, size_t size);` |

* [deck.h](./deck.h): Header file with all definitions and prototypes for the tasks and types created for the `1000-sort_deck.c` task.

Data Structures:
```
typedef enum kind_e
{
    SPADE = 0,
    HEART,
    CLUB,
    DIAMOND
} kind_t;

typedef struct card_s
{
    const char *value;
    const kind_t kind;
} card_t;

typedef struct deck_node_s
{
    const card_t *card;
    struct deck_node_s *prev;
    struct deck_node_s *next;
} deck_node_t;
```

Function Prototype:

| File                | Prototype                          |
| --------------------| -----------------------------------|
| `1000-deck_node.c`  | `void sort_deck(deck_node_t **deck);` |

## Tasks :page_with_curl:

* **0. Bubble Sort**
  * [0-bubble_sort.c](./0-bubble_sort.c): Implements the Bubble Sort algorithm to arrange integers in ascending order within an array.
  * The array is printed after each swap.
  * [0-O](./0-O): A text file listing the best, average, and worst case time complexities for the Bubble Sort algorithm, with each scenario on a separate line.

* **1. Insertion Sort**
  * [1-insertion_sort_list.c](./1-insertion_sort_list.c): Sorts a `listint_t` doubly-linked list of integers in ascending order using the Insertion Sort algorithm.
  * The list is printed after every swap.
  * [1-O](./1-O): A document detailing the best, average, and worst case time complexities for the Insertion Sort algorithm, each on a new line.

* **2. Selection Sort**
  * [2-selection_sort.c](./2-selection_sort.c): Utilizes the Selection Sort algorithm to sort an array of integers in ascending order.
  * The array is displayed after every swap.
  * [2-O](./2-O): Text file with the best, average, and worst case time complexities for the Selection Sort algorithm, presented on individual lines.

* **3. Quick Sort**
  * [3-quick_sort.c](./3-quick_sort.c): Sorts an array of integers in ascending order using the Quick Sort algorithm.
  * Employs the Lomuto partition scheme and always selects the last element of the partition being sorted as the pivot

.
  * The array is printed after each swap.
  * [3-O](./3-O): Document containing the best, average, and worst case time complexities for the Quick Sort Lomuto Partition scheme algorithm, each on a separate line.

* **4. Shell Sort - Knuth Sequence**
  * [100-shell_sort.c](./100-shell_sort.c): Sorts an array of integers in ascending order using the Shell sort algorithm and the Knuth interval sequence.
  * The array is printed every time the interval decreases.

* **5. Cocktail Shaker Sort**
  * [101-cocktail_sort_list.c](./101-cocktail_sort_list.c): Sorts a `listint_t` doubly-linked list of integers in ascending order using the Cocktail Shaker Sort algorithm.
  * The list is printed after each swap.
  * [101-O](./101-O): A text file listing the best, average, and worst case time complexities for the Cocktail Shaker Sort algorithm, with each scenario on its own line.

* **6. Counting Sort**
  * [102-counting_sort.c](./102-counting_sort.c): Employs the Counting Sort algorithm to sort an array of integers in ascending order.
  * Assumes that the array will contain only numbers `>= 0`.
  * The counting array is printed after it has been set up.
  * [102-O](./102-O): Text file with the best, average, and worst case time complexities for the Counting Sort algorithm, each described on a separate line.

* **7. Merge Sort**
  * [103-merge_sort.c](./103-merge_sort.c): Utilizes the Merge Sort algorithm to sort an array of integers in ascending order.
  * Implements a `top-down` Merge Sort algorithm strategy.
    * When dividing an array, the left subarray size is always less than or equal to the right subarray size.
    * The left subarray is always sorted before the right one.
  * Subarrays are printed each time they are merged.
  * [103-O](./103-O): Text file detailing the best, average, and worst case time complexities for the Merge Sort algorithm, with each scenario on its own line.

* **8. Heap Sort**
  * [104-heap_sort.c](./104-heap_sort.c): Sorts an array of integers in ascending order using the Heap Sort algorithm.
  * Implements the `sift-down` Heap Sort method.
  * The array is printed after every swap.
  * [104-O](./104-O): A document containing the best, average, and worst case time complexities for the Heap Sort algorithm, each on a separate line.

* **9. Radix Sort**
  * [105-radix_sort.c](./105-radix_sort.c): Sorts an array of integers in ascending order using the Radix Sort algorithm.
  * Follows the Least-Significant-Digit (LSD) Radix Sort method.
  * Assumes that the array will only contain numbers `>= 0`.
  * The array is printed for each significant digit increase.
  * [105-O](./105-O): Text file with the best, average, and worst case time complexities for the Radix Sort algorithm, each scenario presented on a separate line.

* **10. Bitonic Sort**
  * [106-bitonic_sort.c](./106-bitonic_sort.c): Sorts an array of integers in ascending order using the Bitonic Sort algorithm.
  * Assumes that `size` is a power of 2.
  * Subarrays are printed each time they are merged.
  * [106-O](./106-O): Text file detailing the best, average, and worst case time complexities for the Bitonic Sort algorithm, with each scenario on its own line.

* **11. Quick Sort - Hoare Partition scheme**
  * [107-quick_sort_hoare.c](./107-quick_sort_hoare.c): Sorts an array of integers in ascending order using the Quick Sort algorithm and the Hoare partition scheme.
  * Always selects the last element of the partition being sorted as the pivot.
  * The array is printed after each swap.
  * [107-O](./107-O): A document with the best, average, and worst case time complexities for the Quick Sort Hoare Partition scheme algorithm, each on a separate line.

* **12. Dealer**
  * [1000-sort_deck.c](./1000-sort_deck.c): Sorts a `deck_node_t` doubly-linked list deck of cards.
  * Assumes exactly `52` elements in the doubly-linked list.
  * Orders the deck from spades to diamonds and from aces to kings.