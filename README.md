# Libft - Your Very First Own Library

![cover](cover.png)

*This project has been created as part of the 42 curriculum by acarpent.*

<p align="center">
  <img src="libftm.png" alt="Badge">
</p>

---

## 📋 Description

**Libft** is a foundational C project from the 42 curriculum that involves creating a personal C library containing general-purpose functions. This library serves as a building block for future C projects throughout your programming journey.

The project aims to help you understand how standard C library functions work by implementing them from scratch. You'll learn essential concepts about memory management, string manipulation, linked lists, and proper C programming practices.

### Project Goals

- **Reimplementation of libc functions**: Master the inner workings of standard C functions
- **Memory management**: Learn proper allocation, freeing, and handling of memory
- **Code organization**: Structure a reusable library with clean interfaces
- **Best practices**: Follow the 42 Norm and write robust, efficient code

---

## 🛠️ Instructions

### Compilation

To compile the library and create the static archive file:

```bash
make
```

### Available Make Rules

```bash
make              # Compile the library (creates libft.a)
make all          # Same as make
make clean        # Remove object files (.o)
make fclean       # Remove object files and the library
make re           # Recompile everything (fclean + all)
```

### Using Libft

To use this library in your own projects:

1. Copy the compiled `libft.a` and `libft.h` to your project
2. Include the header in your code:
   ```c
   #include "libft.h"
   ```
3. Compile your project with the library:
   ```bash
   gcc -Wall -Wextra -Werror -o myprogram myprogram.c -L. -lft
   ```

---

## 📚 Library Overview

### Part 1: Libc Functions (Re-implementations)

Character classification functions (return 1 if true, 0 if false):
- `ft_isalpha` - Check if character is alphabetic
- `ft_isdigit` - Check if character is a digit
- `ft_isalnum` - Check if character is alphanumeric
- `ft_isascii` - Check if character is ASCII
- `ft_isprint` - Check if character is printable

Memory manipulation:
- `ft_memset` - Fill memory with a byte value
- `ft_bzero` - Set memory to zero
- `ft_memcpy` - Copy memory area
- `ft_memmove` - Move memory area (handles overlap)
- `ft_memchr` - Locate byte in memory
- `ft_memcmp` - Compare memory areas
- `ft_calloc` - Allocate and initialize memory to zero

String manipulation:
- `ft_strlen` - Get string length
- `ft_strlcpy` - Safely copy string with size
- `ft_strlcat` - Safely concatenate strings with size
- `ft_strchr` - Locate character in string
- `ft_strrchr` - Locate last occurrence of character
- `ft_strncmp` - Compare n bytes of two strings
- `ft_strnstr` - Locate substring within string
- `ft_toupper` - Convert character to uppercase
- `ft_tolower` - Convert character to lowercase
- `ft_atoi` - Convert string to integer
- `ft_strdup` - Duplicate string with malloc

### Part 2: Additional Functions

Advanced string and utility functions:
- `ft_substr` - Extract substring from string
- `ft_strjoin` - Concatenate two strings with malloc
- `ft_strtrim` - Trim characters from start and end of string
- `ft_split` - Split string by delimiter into array
- `ft_itoa` - Convert integer to string
- `ft_strmapi` - Apply function to each character (with index)
- `ft_striteri` - Apply function to each character in-place (with index)
- `ft_putchar_fd` - Write character to file descriptor
- `ft_putstr_fd` - Write string to file descriptor
- `ft_putendl_fd` - Write string with newline to file descriptor
- `ft_putnbr_fd` - Write integer to file descriptor

### Part 3: Linked List Functions

Linked list manipulation using the `t_list` structure:

```c
typedef struct s_list
{
    void            *content;
    struct s_list   *next;
} t_list;
```

Functions:
- `ft_lstnew` - Create a new linked list node
- `ft_lstadd_front` - Add node at the beginning
- `ft_lstadd_back` - Add node at the end
- `ft_lstsize` - Count nodes in list
- `ft_lstlast` - Get the last node
- `ft_lstdelone` - Delete a single node
- `ft_lstclear` - Delete entire list
- `ft_lstiter` - Apply function to each node
- `ft_lstmap` - Apply function and create new list

---

## 🎯 Technical Specifications

### Compilation Requirements

- **Compiler**: `cc` (C compiler)
- **Flags**: `-Wall -Wextra -Werror` (mandatory)
- **Standard C**: No `-std=c99` flag allowed
- **Library creation**: Using `ar` command (NOT libtool)

### Code Standards

- **No global variables** allowed
- **No memory leaks** tolerated
- **Proper memory management**: All allocated memory must be freed
- **No segmentation faults** or unexpected crashes
- **Adherence to 42 Norm**: Required for all source files

### Output

- **Main library**: `libft.a` (static archive)
- **Header file**: `libft.h` (all function prototypes)

---

## 📖 Resources

### C Programming Documentation
- [C Standard Library (cppreference)](https://en.cppreference.com/w/c) - Comprehensive reference for C standard library functions
- [Linux man pages](https://man7.org/linux/man-pages/) - Official Linux manual pages for system calls and functions
- [The C Programming Language (K&R)](https://en.wikipedia.org/wiki/The_C_Programming_Language) - Classic C programming book

### Memory Management
- [Dynamic Memory Allocation in C](https://en.cppreference.com/w/c/memory) - malloc, free, and memory management
- [Understanding Pointers](https://www.geeksforgeeks.org/pointers-in-c-and-c-plus-plus/) - Deep dive into pointer concepts

### Linked Lists
- [Linked List Tutorial](https://www.geeksforgeeks.org/linked-list-set-1-introduction/) - Introduction to linked list concepts
- [Advanced Linked Lists](https://en.cppreference.com/w/cpp/container/list) - More complex linked list operations

### 42 School Resources
- [42 Norm](https://github.com/42School/42cursus/blob/main/docs/en.norm.pdf) - Official 42 coding standard
- [42 Intranet](https://intra.42.fr) - Access to official project guidelines

### How AI Was Used

AI was utilized for **documentation and README creation purposes only**:
- Structuring the README following 42 standards and best practices
- Organizing function descriptions and technical specifications
- Providing clear compilation and usage instructions

**AI was NOT used for**:
- Implementing core C functions
- Writing the library code
- Problem-solving for algorithmic challenges

This aligns with 42's philosophy of building strong foundational knowledge through genuine intellectual effort and peer learning.

---

## 📝 Project Structure

```
libft/
├── Makefile                # Build configuration
├── libft.h                 # Header file with all prototypes
├── ft_*.c                  # Implementation files
├── README.md               # This file
└── Assets
    ├── cover.png           # Project cover image
    └── libftm.png          # Project badge
```

---

## ✅ Verification

To verify that your implementation is working correctly:

1. Compile the library: `make`
2. Create a test program that uses functions from libft
3. Compile your test program with the library
4. Run and verify the output

Example test compilation:
```bash
gcc -Wall -Wextra -Werror -o test test.c -L. -lft
./test
```

---

## 📌 Important Notes

- All functions are prefixed with `ft_` to avoid conflicts with standard C library
- The `restrict` keyword is **NOT used** in any function prototype
- Helper functions are declared as `static` and limited to their file scope
- All submitted files must compile without warnings or errors
- Unused files must not be submitted

---

*Last updated: May 2026*
