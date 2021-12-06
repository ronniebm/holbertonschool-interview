# 0x12. Advanced Binary Search

<!-- badges section with https://img.shields.io/ -->

<span>
  <img src="https://img.shields.io/badge/Specialization-webstack--backend-teal"/>
</span>
&nbsp;&nbsp;

<span>
  <img src="https://img.shields.io/badge/Training-Holberton-red"/>
</span>
&nbsp;&nbsp;

<span>
  <img src="https://img.shields.io/badge/Cohort%20%23-13-yellowgreen"/>
</span>
&nbsp;&nbsp;

<span>
  <img src="https://img.shields.io/badge/Directory-0x12--advanced__binary__search-blue"/>
</span>
<br>
<br>

### TASK

You may have noticed that basic binary search does not necessarily return the index of the first value in the array (if this value appears more than once in the array). In this exercise, you’ll have to solve this problem.

Write a function that searches for a value in a sorted array of integers.

- Prototype : int advanced_binary(int \*array, size_t size, int value);
- array is a pointer to the first element of the array to search in.
- size is the number of elements in array.
- value is the value to search for.
- Your function must return the index where value is located.
- You can assume that array will be sorted in ascending order.
- If value is not present in array or if array is NULL, your function must return -1.
- Every time you split the array, you have to print the new array (or subarray) you’re searching in (See example).
- You have to use recursion. You may only use one loop (while, for, do while, etc.) in order to print the array.

<br>

<pre>
wilfried@0x1D-search_algorithms$ cat 0-main.c 
#include <stdio.h>
#include <stdlib.h>
#include "search_algos.h"

/**
 * main - Entry point
 *
 * Return: Always EXIT_SUCCESS
 */
int main(void)
{
    int array[] = {
        0, 1, 2, 5, 5, 6, 6, 7, 8, 9
    };
    size_t size = sizeof(array) / sizeof(array[0]);

    printf("Found %d at index: %d\n\n", 8, advanced_binary(array, size, 8));
    printf("Found %d at index: %d\n\n", 5, advanced_binary(array, size, 5));
    printf("Found %d at index: %d\n", 999, advanced_binary(array, size, 999));
    return (EXIT_SUCCESS);
}
wilfried@0x1D-search_algorithms$ gcc -Wall -Wextra -Werror -pedantic 0-main.c 0-advanced_binary.c -o 0-advanced_binary
wilfried@0x1D-search_algorithms$ ./0-advanced_binary
Searching in array: 0, 1, 2, 5, 5, 6, 6, 7, 8, 9
Searching in array: 6, 6, 7, 8, 9
Searching in array: 8, 9
Found 8 at index: 8

Searching in array: 0, 1, 2, 5, 5, 6, 6, 7, 8, 9
Searching in array: 0, 1, 2, 5, 5
Searching in array: 5, 5
Found 5 at index: 3

Searching in array: 0, 1, 2, 5, 5, 6, 6, 7, 8, 9
Searching in array: 6, 6, 7, 8, 9
Searching in array: 8, 9
Searching in array: 9
Found 999 at index: -1
</pre>

<!-- Social networks section -->

<br>
<br>
<table>
  <tr>
    <td>
      <img
        src="https://avatars.githubusercontent.com/u/65184918?v=4"
        width="150px"
      />
    </td>
    <td>
      <img
        src="https://github.com/ronniebm/holbertonschool-web_front_end/blob/master/qr-code.png"
        width="150px"
      />
    </td>
  </tr>
</table>

<h3>
  <b>👋 Hi, I'm Ronnie Barrios.
  </b>
</h3>
____________________________________
<br>
Let's get in touch !, scan QR code.
<br><br>

<a href="https://twitter.com/ronniealberto">
  <img 
    src="https://pics.freeicons.io/uploads/icons/png/20422544081555590088-512.png"
    width="30px"
  />
</a>
&emsp;

<a href="https://www.linkedin.com/in/ronniebm/">
  <img 
    src="https://pics.freeicons.io/uploads/icons/png/15792152941556105325-512.png"
    width="30px"
  />
</a>
&emsp;

<a href="https://github.com/ronniebm/">
  <img 
    src="https://pics.freeicons.io/uploads/icons/png/13702699181561032680-512.png"
    width="30px"
  />
</a>
&emsp;
<br>
<a href="mailto:ronnie.coding@gmail.com?subject=Let's do a meet ! &amp;body=Hi Ronnie, %0D%0A%0D%0A I've check your Github profile, i would like to contact you.%0D%0A%0D%0A Att,%0D%0A------------------------%0D%0A***your sign*** &amp;">
<br>
--->&emsp;or Send EMAIL here&emsp;<---
</a>
