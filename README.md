# 1337-libft

## Overview
The libft project is a custom C library that provides a collection of useful functions for C programming. It is a common beginner project at 42 that helps you learn about low-level programming.

## Core Concepts
  - File descriptors
  - Typecasting
  - Linked lists
  - Pointers
  - Data structures
  - Memory management
  - Integer overflow or wraparound

## Getting started
  1. Clone this repository
       ```bash
       git clone https://github.com/akarichan00/1337-libft.git
       ```
  2. Enter the repository and Compile the files using make:
      ```bash
      cd 1337-libft
      make
      ```
  3. Use it in your code
     To use the library functions in your code, clone it in your project's root folder and simply include its header:
     ```bash
     #include "libft.h"
     ```

## Resources
  - [Understanding Makefile](https://www.youtube.com/watch?v=a8mPKBxQ9No&t=55s)
  - [Memory Management in C](https://www.geeksforgeeks.org/dynamic-memory-allocation-in-c-using-malloc-calloc-free-and-realloc/)
  - [Linked Lists](https://www.youtube.com/watch?v=vcQIFT79_50&t=1s)
  - [Data structures](https://www.w3schools.com/c/c_structs.php) 


# Tester
  To test your Libft -> use this tester : https://github.com/xicodomingues/francinette

# Notes
## Why Use Double Pointers in Linked Lists?
 - In C, everything, including pointers, is passed by value. This means that if you pass a pointer to a function, you are passing a copy of the pointer, not the original. To modify the pointer itself (e.g., add a new element to the front of a list), you need to pass a pointer to the pointer, i.e., a double pointer.
 - Here’s how double pointers work in the context of a linked list:
     ```bash
       void ft_lstadd_front(t_list **lst, t_list *new)
      {
        if (lst && new)
        {
            new->next = *lst;
            *lst = new;
        }
      }
       ```
  - In the ft_lstadd_front function, we modify the original pointer to point to the new element by using a double pointer.
