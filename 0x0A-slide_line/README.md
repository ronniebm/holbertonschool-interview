# 0x0A. 2048 (single line)

<!-- badges section with https://img.shields.io/ -->

<span>
  <img src="https://img.shields.io/badge/Specialization-webstack--frontend-green"/>
</span>
&nbsp;&nbsp;

<span>
  <img src="https://img.shields.io/badge/Training-Holberton-red"/>
</span>
&nbsp;&nbsp;

<span>
  <img src="https://img.shields.io/badge/Cohort%20%23-12-yellowgreen"/>
</span>
&nbsp;&nbsp;

<span>
  <img src="https://img.shields.io/badge/Directory-0x0A--slide__line-blue"/>
</span>
<br>
<br>

<!-- image and subtitle section -->

<img
  src="https://image.flaticon.com/icons/png/512/90/90603.png"
  width="150px"
/>

<br>

<!-- Learning objectives section -->

## **EXCERCISE**

The goal of this task is to reproduce the 2048 game(NSFW !!) mechanics on a single horizontal line.

Given an array of integers, we want to be able to slide & merge it to the left or to the right. Identical numbers, if they are contiguous or separated by zeros, should be merged (See example)

- Write a function that slides and merges an array of integers
- Prototype: <code>int slide_line(int *line, size_t size, int direction);</code>
- Where <code>line</code> points to an array of integers containing <code>size</code> elements, that must be slided & merged to the direction represented by <code>direction</code>. <code>direction</code> can be either:
  - <code>SLIDE_LEFT</code>
  - <code>SLIDE_RIGHT</code>
  - If it is something else, the function must fail
  - Both macros <code>SLIDE_LEFT</code> and <code>SLIDE_RIGHT</code> must be defined in <code>slide_line.h</code>
- Your function must return 1 upon success, or 0 upon failure
- You are not allowed to allocate memory dynamically (malloc, calloc, …) 
<br>
<br>

# code testing
<pre>
alex@~/0x0A-slide_line$ cat 0-main.c 
#include <stdlib.h>
#include <stdio.h>

#include "slide_line.h"

#define LINE_SIZE   32

/**
 * print_array - Prints out an array of integer, followed by a new line
 * 
 * @array: Pointer to the array of integer to be printed
 * @size: Number of elements in @array
 */
static void print_array(int const *array, size_t size)
{
    size_t i;

    printf("Line: ");
    for (i = 0; i < size; i++)
        printf("%s%d", i > 0 ? ", " : "", array[i]);
    printf("\n");
}

/**
 * main - Entry point
 *
 * @ac: Arguments counter
 * @av: Arguments vector
 *
 * Return: EXIT_SUCCESS or EXIT_FAILURE
 */
int main(int ac, char **av)
{
    int line[LINE_SIZE];
    int direction;
    size_t i, size;

    if (ac < 3)
    {
        fprintf(stderr, "Usage: %s <R/L> <n1> [n2...]\n", av[0]);
        return (EXIT_FAILURE);
    }

    /* Command line arguments to array of int */
    size = ac - 2;
    if (size > LINE_SIZE)
        size = LINE_SIZE;
    for (i = 0; i < size; i++)
        line[i] = atoi(av[i + 2]);

    /* Print the array */
    print_array(line, size);

    /* Parse direction */
    switch (*(av[1]))
    {
    case 'L':
        direction = SLIDE_LEFT;
        printf("Slide to the left\n");
        break;
    case 'R':
        direction = SLIDE_RIGHT;
        printf("Slide to the right\n");
        break;
    default:
        fprintf(stderr, "Unknown direction '%c'. Please use 'L' or 'R'", *(av[1]));
        return (EXIT_FAILURE);
    }

    /* Slide and merge */
    if (!slide_line(line, size, direction))
    {
        fprintf(stderr, "Failed to slide and merge line\n");
        return (EXIT_FAILURE);
    }

    /* Print the array */
    print_array(line, size);

    return (EXIT_SUCCESS);
}
alex@~/0x0A-slide_line$ gcc -Wall -Wextra -Werror -pedantic -o 0-slide_line 0-main.c 0-slide_line.c
alex@~/0x0A-slide_line$ ./0-slide_line L 2 2 0 0
Line: 2, 2, 0, 0
Slide to the left
Line: 4, 0, 0, 0
alex@~/0x0A-slide_line$ ./0-slide_line L 2 2 0 0 0 0 0 2 0 0 0 2 0 4
Line: 2, 2, 0, 0, 0, 0, 0, 2, 0, 0, 0, 2, 0, 4
Slide to the left
Line: 4, 4, 4, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0
alex@~/0x0A-slide_line$ ./0-slide_line R 2 2 2 2
Line: 2, 2, 2, 2
Slide to the right
Line: 0, 0, 4, 4
alex@~/0x0A-slide_line$ ./0-slide_line R 2 2 2 2 2
Line: 2, 2, 2, 2, 2
Slide to the right
Line: 0, 0, 2, 4, 4
alex@~/0x0A-slide_line$ ./0-slide_line L 2 4 8 16
Line: 2, 4, 8, 16
Slide to the left
Line: 2, 4, 8, 16
alex@~/0x0A-slide_line$ ./0-slide_line R 2 4 8 16
Line: 2, 4, 8, 16
Slide to the right
Line: 2, 4, 8, 16
alex@~/0x0A-slide_line$ ./0-slide_line R 4 4 8 16
Line: 4, 4, 8, 16
Slide to the right
Line: 0, 8, 8, 16
alex@~/0x0A-slide_line$
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
