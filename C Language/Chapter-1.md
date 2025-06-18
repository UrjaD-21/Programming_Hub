# **🌟 Chapter-1: C Programming Basics**

**📚 Topics Covered:**
- 🧠 Variables

- 🔑 Keywords

- 📏 Constants

- 💬 Comments

- 🏗️ Structure

- ⚙️ Compilation

## **🧠 Variables** 
> **🔸 What is a Variable?**
>> Variable is the name of a memory location which stores some data.
> _Imagine your computer's memory as a row of boxes 🧊🧊🧊,and each variable is a label stuck on a box to help you find or change its contents later._

  **Memory**
   
```
    ------+------+------+------+------+------+------+------+
    |     |      |      |  25  |      |      |  S   |      |
    ------+------+------+------+------+------+------+------+
                            a                    b
```
          
- a = 25 ➡️ 🎯 Integer value stored
- b = 'S' ➡️ 🔤 Character stored


🧪 Code Example: Declaring Variables in C

  ```c
#include <stdio.h>

int main() {
    int a = 25;         // 🧠 "a" stores integer 25
    char star = '*';    // 🌟 "star" stores character '*'
    int age = 19;       // 👶 "age" stores integer 19
    float pi = 3.14;    // 🥧 "pi" stores float 3.14
    return 0;
}

  ```
**💡 Tips to Remember:**

_- Variable names should be meaningful (like age, pi, total)._

_- Data type must match the kind of value you want to store (like int, char, float)._

_- Always initialize variables to avoid garbage values 🗑️._


> ## Rules :

> - Variables are case sensitive
> - 1st character is alphabet or '_'
> - No comma/blank space
> - No other symbol except '_'

> ## 📏 C Data Types and Their Sizes (in Bytes)
> A handy reference table for sizes of various C data types 💻📚:
> 
> | 🧾 **Data Type**                        | 📦 **Size (Bytes)** |
> |-----------------------------------------|---------------------|
> | 🔤 Char or signed char                  | 1                   |
> | 🔡 Unsigned char                        | 1                   |
> | 🔢 int or signed int                    | 2                   |
> | ➕ Unsigned int                         | 2                   |
> | 🔽 Short int or Unsigned short int      | 2                   |
> | 🧮 Signed short int                     | 2                   |
> | 📏 Long int or Signed long int          | 4                   |
> | 🧾 Unsigned long int                    | 4                   |
> | 🌊 float                                | 4                   |
> | 🌐 double                               | 8                   |
> | 💎 Long double                          | 10                  |

---

## **🔒Constants in C**

>> 🧊 Constants are fixed values in a program that do not change during execution.
_They are like permanent labels on memory 🧠 — once assigned, they stay the same throughout the program!_

```sql
               +-------------------------+
               |       Constants         |
               | (Fixed Values in C 💡)  |
               +-----------+-------------+
                           |
          +----------------+----------------+
          |                                 |
  +-------v-------+                 +--------v---------+
  | Integer       |                 | Character        |
  | Constants     |                 | Constants        |
  +---------------+                 +------------------+
  | Examples:     |                 | Examples:        |
  | 1, 2, 3, 0    |                 | 'a', 'b', 'A'    |
  | -1, -2        |                 | '#', '&'         |
  +---------------+                 +------------------+
          |
          |
  +-------v--------+
  | Real Constants |
  +----------------+
  | Examples:      |
  | 1.0, 2.0, 3.14 |
  | -24.0          |
  +----------------+

```

---

## **🔑 Keywords**

>> 🔐 Keywords are reserved words in C that have special meaning to the compiler.
_They cannot be used as variable names, function names, or identifiers because they are predefined by the language itself._

**🎯 Key Fact:**
- 🧾 There are exactly **32 Keywords** in C 🧑‍💻

```
📜 Examples of Keywords in C:

auto      break     case      char     const
continue  default   do        double   else
enum      extern    float     for      goto
if        int       long      register return
short     signed    sizeof    static   struct
switch    typedef   union     unsigned void
volatile  while

```

**🧭 Why are Keywords Important?**
- 🛠️ They define the structure and rules of the C language

- 🎯 Without them, the compiler wouldn’t understand what you want to do

- 🚫 You can't redefine or modify them

---

## **💬 Comments**

>> 
  
