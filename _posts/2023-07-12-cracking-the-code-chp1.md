---
title: "Cracking the Code Interview Chapter 1"
date: 2023-07-12
categories:
  - tech
tags:
  - Programming
  - CCI
---

## Chapter1: Arrays and Strings

McDowell, long before I even started this blog.

Actually, I started this blog because of this book. 😅

So here it is. I will now cover the first chapter which starts with Arrays and Strings but explains something completely different. Starting with...

### Hash Tables
It is a data structure that stores key/value pairs for a highly efficient lookup. In Python, this type of structure is found in dictionaries and sets.

They are so efficient that in the book by Luciano Ramalho (Fluent Python), he experimented using both dict() and set().

The experiment consisted of two arrays. One with 10 million unique numbers (the haystack) and another with 1.000 numbers (the needles), in which 500 elements were in the haystack, 500 weren't.

Then, he applied the dict, set, and list method to measure the time it would take to find the elements of the needles in the haystack.

For the array containing 10 million numbers, the respective times for each method were:

- dict: 0,000337 seconds
- set: 0,000387 seconds
- list: 97,948056 seconds

So, yeah. Hash tables make the lookup search much much faster.

But even with that, we can solve the permutation questions from the book without resorting to it and still be on O(n) time complexity.

For example, question 1.2 states:
*Given two strings, write a method to decide if one is a permutation of the other.*

One way to solve it would be:

````Python
def is_permutation(str1, str2):
    #1
    if len(str1) != len(str2):
        return False
    #2
    char_count = [0] * 128

    #3
    for char in str1:
        char_count[ord(char)] += 1

    #4
    for char in str2:
        char_count[ord(char)] -= 1
        if char_count[ord(char)] < 0:
            return False

    return True
````

In 1, we check if the strings have a different length if so, they can't be a permutation of the other.

Next (2), we create a zero-filled array for the 128 ASCII characters. 

In 3, we fill the char_count variable with a one for each position that the ord() function returns for each character in `str1`. 

The function ord() return the ASCII value of a given character.

Finally, in 4 we decrement the count of each character in `char_count` using the same logic.

If the count becomes negative, it means `str2` has more occurrences of that character than `str1`, and we return `False`. If it returns zero, it means that the arrays are a permutation of each other.

### Array List and Resizable Arrays

Arrays or lists are automatically resizable. To append a value or a list of values to a Python list the time complexity will always remain O(1).

Since we are adding values to the end of the array, the method doesn't need to know the length  of the list.

### StringBuilder

This class comes from Java since strings are immutable in this language.
Now for Python, there are numerous ways that you can alter a string. 

For example, for question 1.6: *Implement a method to perform basic string compression using the counts of repeated characters.* Can be solved by:

````Python
def string_compression(s):
    #1
    compressed_string = ""
    #2
    count = 1
    #3
    for i in range(1, len(s)):
        if s[i] == s[i-1]:
            count += 1
        else:
            compressed_string += s[i-1] + str(count)
            count = 1

    compressed_string += s[-1] + str(count)

    #4
    if len(compressed_string) < len(s):
        return compressed_string
    else:
        return s
````

In 1, we define an empty string to hold our compressed result.

Then in 2, we start a counter for 1, since there will be a least one character of each.

The for loop in 3 will compare the next character with the previous one. If the value is the same, we add one to `count` to keep track of how many there are. If not, we append it to the `compressed_string` variable along with the counter. 

Finally, on 4, we compare both strings' lengths. If the `compressed_string` is smaller than the original one, we return the `compressed_string`. If not, we return the original one, since it's already the most compressed way that it can be displayed.

In conclusion, arrays and strings in Python are pretty handy when it comes to data manipulation.

Next chapter will be about Linked Lists. You can check all the solutions for this chapter's questions in my GitHub [Repo](https://github.com/Isabela192/Coding_Interview).

Todaloo!