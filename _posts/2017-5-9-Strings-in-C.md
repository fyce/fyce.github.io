---
layout: post
title:  Strings in C
---

In C, strings are null-terminated character arrays. This means the last element of a string array contains '/0'.
Being arrays, a string variable *acts* as a pointer to a character (sequence of characters), so array resembles pointer arithmetic .
A character array variable name when reference by itself (without any index), points to the first element of the character array, with index number 0.

A library function, say printf (with a format specifier "%s"), expects a character array, and will print out all characters before the first null character '0/'. For example:

	char charArray[] = {'0/', 'b', 'e', '0/'}; 
	printf("%s", charArray); 

The above example will print no character as null is encountered at charArray[0].

	printf("%s", charArray + 1); 

However, this second example prints "be" because the charArray pointer(base address, which printf("%s") expects) is incremented to 'b'. 

Just when I thought I got the relationship between arrays and pointers, I read [section 6 of the comp.lang.c FAQ](http://www.c-faq.com/aryptr/index.html). You should read it too!

## Related links
[C strings, pointers, memory addresses etc.](http://denniskubes.com/category/c/)

[Section 6 of the comp.lang.c FAQ](http://www.c-faq.com/aryptr/index.html)
