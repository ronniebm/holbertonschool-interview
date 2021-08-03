# 0x09. UTF-8 Validation

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
  <img src="https://img.shields.io/badge/Directory-0x09--utf8__validation-blue"/>
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

Write a method that determines if a given data set represents a valid UTF-8 encoding.

-  Prototype: def validUTF8(data).  
-  Return: True if data is a valid UTF-8 encoding, else return False.  
-  A character in UTF-8 can be 1 to 4 bytes long.  
-  The data set can contain multiple characters.  
-  The data will be represented by a list of integers.  
-  Each integer represents 1 byte of data, therefore you only need to handle the 8 least -  significant bits of each integer.  
<br>
<br>

# code testing
<pre>
carrie@ubuntu:~/0x09-utf8_validation$ cat 0-main.py
#!/usr/bin/python3
"""
Main file for testing
"""

validUTF8 = __import__('0-validate_utf8').validUTF8

data = [65]
print(validUTF8(data))

data = [80, 121, 116, 104, 111, 110, 32, 105, 115, 32, 99, 111, 111, 108, 33]
print(validUTF8(data))

data = [229, 65, 127, 256]
print(validUTF8(data))

carrie@ubuntu:~/0x09-utf8_validation$
</pre>

<br>

<pre>
carrie@ubuntu:~/0x09-utf8_validation$ ./0-main.py
True
True
False
carrie@ubuntu:~/0x09-utf8_validation$
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
