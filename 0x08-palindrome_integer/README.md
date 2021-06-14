# 0x08. Palindrome integer

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
  <img src="https://img.shields.io/badge/Directory-0x08--palindrome__integer-blue"/>
</span>
<br>
<br>

<!-- image and subtitle section -->

<img
  src="https://image.flaticon.com/icons/png/512/90/90603.png"
  width="150px"
/>

<br>

## [0. Palindrome unsigned integer](./0-is_palindrome.c)
Write a function that checks whether or not a given unsigned integer is a palindrome.

- Prototype: `int is_palindrome(unsigned long n);`
- Where n is the number to be checked
- Your function must return 1 if n is a palindrome, and 0 otherwise
- You are not allowed to allocate memory dynamically (malloc, calloc, …)
```
alex@~/0x08-palindrome_integer$ cat 0-main.c
#include <stdlib.h>
#include <stdio.h>

#include "palindrome.h"

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
    unsigned long n;
    int ret;

    if (ac < 2)
    {
        fprintf(stderr, "Usage: %s arg\n", av[0]);
        return (EXIT_FAILURE);
    }

    n = (unsigned long)(atol(av[1]));
    ret = is_palindrome(n);

    printf("%lu is ", n);
    if (ret == 0)
        printf("not ");
    printf("a palindrome.\n");

    return (EXIT_SUCCESS);
}
alex@~/0x08-palindrome_integer$ gcc -Wall -Wextra -Werror -pedantic -g3 -o palindrome 0-main.c 0-is_palindrome.c
alex@~/0x08-palindrome_integer$ ./palindrome 1
1 is a palindrome.
alex@~/0x08-palindrome_integer$ ./palindrome 11
11 is a palindrome.
alex@~/0x08-palindrome_integer$ ./palindrome 112
112 is not a palindrome.
alex@~/0x08-palindrome_integer$ ./palindrome 121
121 is a palindrome.
alex@~/0x08-palindrome_integer$ ./palindrome 12345678987654321
12345678987654321 is a palindrome.
alex@~/0x08-palindrome_integer$ ./palindrome 123456789987654321
123456789987654321 is a palindrome.
alex@~/0x08-palindrome_integer$ ./palindrome 1234567898654321
1234567898654321 is not a palindrome.
alex@~/0x08-palindrome_integer$
```

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
