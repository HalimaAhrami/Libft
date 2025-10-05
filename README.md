
---

# **Libft**

## **Project Name**

`libft.a`

## **Objective**

Create a personal C library implementing standard C functions and additional useful utilities. This library serves as a foundation for future C projects.

---

## **Project Structure**

* **Files to submit:**

  * `Makefile`
  * `libft.h`
  * `ft_*.c` (function implementations)
* **Makefile Requirements:**

  * Compile with flags `-Wall -Wextra -Werror`
  * Must include rules: `NAME`, `all`, `clean`, `fclean`, `re`
  * Bonus functions should have a separate `bonus` rule
* **Library Creation:**

  * Use `ar` to create `libft.a`
  * Global variables forbidden
  * Helper functions must be `static` if not used externally
* **Memory Management:**

  * All heap memory must be properly freed
  * Segmentation faults, double frees, or undefined behavior result in 0

---

## **Mandatory Part – Functions**

### **Part 1 – Reimplementing Libc Functions**

Functions must behave like standard C library functions but with prefix `ft_`.

| Function     | Purpose                                        |
| ------------ | ---------------------------------------------- |
| `ft_isalpha` | Check if character is alphabetic               |
| `ft_isdigit` | Check if character is a digit                  |
| `ft_isalnum` | Check if character is alphanumeric             |
| `ft_isascii` | Check if character is ASCII                    |
| `ft_isprint` | Check if character is printable                |
| `ft_strlen`  | Get length of a string                         |
| `ft_memset`  | Fill memory with a constant byte               |
| `ft_bzero`   | Set memory to zero                             |
| `ft_memcpy`  | Copy memory from source to destination         |
| `ft_memmove` | Copy memory safely (handles overlap)           |
| `ft_strlcpy` | Copy string to buffer with size limit          |
| `ft_strlcat` | Concatenate string with size limit             |
| `ft_toupper` | Convert character to uppercase                 |
| `ft_tolower` | Convert character to lowercase                 |
| `ft_strchr`  | Locate first occurrence of character in string |
| `ft_strrchr` | Locate last occurrence of character in string  |
| `ft_strncmp` | Compare two strings up to n characters         |
| `ft_memchr`  | Search memory for a byte                       |
| `ft_memcmp`  | Compare memory blocks                          |
| `ft_strnstr` | Locate substring in string with size limit     |
| `ft_atoi`    | Convert string to integer                      |
| `ft_calloc`  | Allocate zero-initialized memory               |
| `ft_strdup`  | Duplicate a string                             |

**Notes:**

* `calloc` and `strdup` require `malloc`.
* Behavior must match the man page.

---

### **Part 2 – Additional Functions**

| Function        | Purpose                                       | Parameters                            | Return Value            |
| --------------- | --------------------------------------------- | ------------------------------------- | ----------------------- |
| `ft_substr`     | Create substring                              | Original string, start index, length  | Substring               |
| `ft_strjoin`    | Join two strings                              | String1, String2                      | New concatenated string |
| `ft_strtrim`    | Trim characters from start/end                | Original string, characters to remove | Trimmed string          |
| `ft_split`      | Split string by delimiter                     | Original string, delimiter            | Array of strings        |
| `ft_itoa`       | Convert integer to string                     | Integer                               | String representation   |
| `ft_strmapi`    | Map function over string, creating new string | Original string, function             | New string              |
| `ft_striteri`   | Apply function to string in-place             | Original string, function             | None                    |
| `ft_putchar_fd` | Output character to file descriptor           | Character, fd                         | None                    |
| `ft_putstr_fd`  | Output string to file descriptor              | String, fd                            | None                    |
| `ft_putendl_fd` | Output string with newline                    | String, fd                            | None                    |
| `ft_putnbr_fd`  | Output integer                                | Integer, fd                           | None                    |

---

## **Bonus Part – Linked Lists**

**Node Structure:**

* `content`: Data stored (any type)
* `next`: Pointer to next node (NULL if last)

**Functions:**

| Function          | Purpose                                                 |
| ----------------- | ------------------------------------------------------- |
| `ft_lstnew`       | Create a new node                                       |
| `ft_lstadd_front` | Add node at the beginning                               |
| `ft_lstadd_back`  | Add node at the end                                     |
| `ft_lstsize`      | Count nodes in list                                     |
| `ft_lstlast`      | Return last node                                        |
| `ft_lstdelone`    | Delete node using a given function                      |
| `ft_lstclear`     | Delete all nodes starting from given node               |
| `ft_lstiter`      | Apply function to each node content                     |
| `ft_lstmap`       | Apply function to content of each node, create new list |

**Notes:**

* Bonus evaluated **only if mandatory part is perfect**
* Memory management with `malloc` and `free` is crucial

---

## **Evaluation Notes**

* Mandatory and bonus functions are graded separately
* Peer evaluation may request small modifications
* Library will be a core tool in all future projects

---