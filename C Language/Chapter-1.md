# **🌟 Chapter-1: C Programming Basics**

**📚 Topics Covered:**
- 🧠 Variables

- 🔑 Keywords

- 📏 Constants

- 💬 Comments

- 🏗️ Structure [Click Here to learn more!!](https://github.com/UrjaD-21/Programming_Hub/blob/main/C%20Language/Structure-of-C.md)

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


> ### ***Rules :***
> - Variables are case sensitive
> - 1st character is alphabet or '_'
> - No comma/blank space
> - No other symbol except '_'

> ### ***📏 C Data Types and Their Sizes (in Bytes)***
> A handy reference table for sizes of various C data types 💻📚:
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

## **💬 Comments & Documentation**

***📚 1. What are Comments in C?***
>> 🗣️ Comments are non-executable statements that help explain your code.
They are ignored by the compiler, meaning they don’t affect your program’s output or logic.

--

***📌 2. Why Use Comments?***

| Purpose              | Benefit                                 |
| -------------------- | --------------------------------------- |
| 📖 Explain the code  | Helps you and others understand logic   |
| 🧪 Debug the code    | Temporarily disable code blocks         |
| 🧠 Self-reminder     | Future-you will thank you!              |
| 📄 Add documentation | Attach program info, like author & date |

--

***📋 3. Types of Comments***
  
**🟦 Single-line Comment (`//`)**
- Starts with // and goes till the end of the line.
- Best for short notes or explaining a line.
  
- ```c
  #include <stdio.h>
  int main() {
    int side = 5; // Length of one side of square
    int area = side * side; // Calculating area
    printf("Area = %d", area);
    return 0;
  }
  ```
--

**🟩 Multi-line Comment (`/* ... */`)**
- Can span multiple lines.
- Great for explaining large blocks or adding documentation.

- ```c
  /*
    Program: Area Calculator
    Author: Urja Doshi
    Created on: 18-06-2025
    Description: This program calculates the area of a square.
  */
  #include <stdio.h>
  int main() {
    int side = 4;
    int area = side * side;
    printf("Area = %d", area);
    return 0;
  }
  ```
--

  ***📝 4. Documentation Using Comments***

  >> Documentation is a special comment section at the top of your program that includes:

| 🔍 Detail    | 🧾 Example                     |
| ------------ | ------------------------------- |
| Program Name | Area Calculator                 |
| Description  | Calculates the area of a square |
| Programmer   | Urja Doshi                      |
| Date & Time  | 18-06-2025, 9:00 PM             |


*📌 Recommended Format (Multi-line)*

```c
/*
    📌 Program: Area Calculator
    📌 Author: Urja Doshi
    📌 Date: 18-06-2025
    📌 Description: Calculates area of a square using side*side
*/
```

*📌 Alternative Format (Single-line)*

```c
// Program: Area Calculator | Author: Urja | Date: 18-06-2025
```
--

**⚠️ Common Mistakes to Avoid**

❌ Writing incorrect/outdated comments.

❌ Over-commenting obvious code:

```c
int x = 10; // x is 10 → (Too obvious!)
```
❌ Forgetting to update the author/date in documentation.

--

**🛠️ Practice Challenge**

🧩 Try writing documentation and comments for this program:

```c
#include <stdio.h>
int main() {
    int a = 6, b = 3;
    int product = a * b;
    printf("Product = %d", product);
    return 0;
}
```

---

## ****

***💡 What is Compilation?***
>> 🧠 Compilation is the process of converting your C source code (human-readable) into machine code (computer-understandable) so the program can be executed.
>> It is done using a special program called a compiler.

--

**🔄 Compilation Cycle in C**
- The process happens in multiple stages, not just one "magic" step.
Here’s the full journey from your .c file to the output:

- ```
       ┌────────────┐      ┌────────────┐      ┌────────────┐      ┌────────────┐
     │  Source    │ ---> │  Preprocessor│ --->│ Compiler    │ --->│ Linker      │
     │  Code (.c) │      │  (e.g., #include)│   │ (Assembly code)│   │ (Executable)│
     └────────────┘      └────────────┘      └────────────┘      └────────────┘
  ```

--
  
**🔍 Compilation Stages (Simplified)**

| Stage            | What Happens                              | File Generated                            |
| ---------------- | ----------------------------------------- | ----------------------------------------- |
| 🛠 Preprocessing | Handles `#include`, `#define`, etc.       | `.i` file                                 |
| 🧬 Compilation   | Converts preprocessed code to Assembly    | `.s` file                                 |
| 🧱 Assembling    | Assembles into Machine code (Object File) | `.o` or `.obj` file                       |
| 🔗 Linking       | Combines all code and libraries           | `.exe` (on Windows) or executable (Linux) |

--

**🗂️ Example with gcc Compiler (Linux)*

Suppose you have a file named program.c.

```bash
gcc program.c -o program
```

- `gcc` → the compiler

- `program.c` → your source file

- `-o program` → tells compiler the output file should be named program

- To run the program:
```bash
./program
```
🖥️ Output will be displayed on terminal!

--

**🧠 Quick Tip: Use Comments for Compilation Info**

You can also document the compile command like this:
```c
/*
    To compile this program:
    gcc area.c -o area
    ./area
*/
```
> ***✅ Example Code:***
> ```c
> /*
    Program: Addition
    Author: Urja Doshi
    Date: 18-06-2025
    Description: Demonstrates compilation of a simple program.
    To compile: gcc addition.c -o addition
    */
    
    #include <stdio.h>
    int main() {
      int a = 5, b = 7;
      int sum = a + b;
      printf("Sum = %d", sum);
      return 0;
     }

--

**⚠️ Common Errors During Compilation**

| Error                 | Cause                                  |
| --------------------- | -------------------------------------- |
| `undefined reference` | Missing function or not linked         |
| `missing semicolon`   | Syntax error                           |
| `undeclared variable` | Variable used before declaration       |
| `missing header`      | Forgot to `#include` necessary library |

--

**🧩 Mini Exercise**

- Write and compile a program to:

- Multiply two numbers

- Document it properly with compilation steps





  
