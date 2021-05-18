# 0x04. Sandpiles

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
  <img src="https://img.shields.io/badge/Directory-0x04--sandpiles-blue"/>
</span>
<br>
<br>

<!-- image and subtitle section -->

<img
  src="https://image.freepik.com/free-vector/pile-sand-cartoon-set-icon-illustration-sandy-mound_158626-549.jpg"
  width="150px"
/>

## **Forms** 👔

<br>

<!-- Learning objectives section -->

## **EXCERCISE**

Write a function that computes the sum of two sandpiles.  

Prototype: <pre>void sandpiles_sum(int grid1[3][3], int grid2[3][3]);</pre>
- You can assume that both grid1 and grid2 are individually stable.  
- A sandpile is considered stable when none of its cells contains more than 3 grains.  
- When your function is done, grid1 must be stable.  
- grid1 must be printed before each toppling round, only if it is unstable (See example).  
- You’re not allowed to allocate memory dynamically.  
  <br>

# code testing
<pre>
alex@~/0x04-sandpiles$ cat 0-main.c 
#include <stdlib.h>
#include <stdio.h>

#include "sandpiles.h"

/**
 * print_grid_sum - Print 3x3 grids sum
 * @grid1: Left 3x3 grid
 * @grid2: Right 3x3 grid
 *
 */
static void print_grid_sum(int grid1[3][3], int grid2[3][3])
{
    int i, j;

    for (i = 0; i < 3; i++)
    {
        for (j = 0; j < 3; j++)
        {
            if (j)
                printf(" ");
            printf("%d", grid1[i][j]);
        }

        printf(" %c ", (i == 1 ? '+' : ' '));

        for (j = 0; j < 3; j++)
        {
            if (j)
                printf(" ");
            printf("%d", grid2[i][j]);
        }
        printf("\n");
    }
}

/**
 * print_grid - Print 3x3 grid
 * @grid: 3x3 grid
 *
 */
static void print_grid(int grid[3][3])
{
    int i, j;

    for (i = 0; i < 3; i++)
    {
        for (j = 0; j < 3; j++)
        {
            if (j)
                printf(" ");
            printf("%d", grid[i][j]);
        }
        printf("\n");
    }
}

/**
 * main - Entry point
 *
 * Return: EXIT_SUCCESS or EXIT_FAILURE
 */
int main(void)
{
    int grid1[3][3] = {
        {3, 3, 3},
        {3, 3, 3},
        {3, 3, 3}
    };
    int grid2[3][3] = {
        {1, 3, 1},
        {3, 3, 3},
        {1, 3, 1}
    };

    print_grid_sum(grid1, grid2);

    sandpiles_sum(grid1, grid2);

    printf("=\n");
    print_grid(grid1);

    return (EXIT_SUCCESS);
}
alex@~/0x04-sandpiles$ gcc -Wall -Wextra -Werror -pedantic 0-main.c 0-sandpiles.c -o 0-sandpiles
alex@~/0x04-sandpiles$ ./0-sandpiles 
3 3 3   1 3 1
3 3 3 + 3 3 3
3 3 3   1 3 1
=
4 6 4
6 6 6
4 6 4
=
2 5 2
5 6 5
2 5 2
=
4 2 4
2 6 2
4 2 4
=
0 5 0
5 2 5
0 5 0
=
2 1 2
1 6 1
2 1 2
=
2 2 2
2 2 2
2 2 2
alex@~/0x04-sandpiles$ cat 1-main.c
Same as 0-main.c except:
int grid1[3][3] = {
        {0, 0, 0},
        {0, 0, 0},
        {0, 0, 0}
    };
    int grid2[3][3] = {
        {3, 3, 3},
        {3, 3, 3},
        {3, 3, 3}
    };
alex@~/0x04-sandpiles$ gcc -Wall -Wextra -Werror -pedantic 1-main.c 0-sandpiles.c -o 0-sandpiles
alex@~/0x04-sandpiles$ ./0-sandpiles 
0 0 0   3 3 3
0 0 0 + 3 3 3
0 0 0   3 3 3
=
3 3 3
3 3 3
3 3 3
alex@~/0x04-sandpiles$
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
