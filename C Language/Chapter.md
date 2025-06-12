# 🔹 Structure of a C Program

A C program is typically divided into six sections:

## 1. **Documentation**
   - Includes:
     - Description of the program
     - Name of the program
     - Programmer's name
     - Date and time of creation
   - Placed at the top of the program as comments.
   - **Single-line comment**: `//`
   - 
     ```c
     // Program to calculate area, Author: ABC, Date: xx-xx-xxxx
     ```
     
   - **Multi-line comment**: `/* ... */`
     ```c
     /*
        Program to calculate area
        Author: ABC
        Date: xx-xx-xxxx
     */
     ```

---

## 2. **🔷 C Preprocessor in Detail**

<details>
<summary><strong>
The  is a tool that is executed before the actual compilation of code begins.</strong></summary>
  
It processes directives that begin with the `#` symbol. These directives tell the compiler to: 

- Include files  
- Define constants/macros  
- Conditionally compile code

### 🔹 Types of Preprocessor Directives

| Directive | Purpose                        | Example                   |
|----------|--------------------------------|---------------------------|
| `#include` | Includes header files         | `#include <stdio.h>`      |
| `#define`  | Defines macros or constants   | `#define PI 3.14`         |
| `#undef`   | Undefines a macro             | `#undef PI`               |
| `#ifdef`   | If macro is defined           | `#ifdef DEBUG`            |
| `#ifndef`  | If macro is not defined       | `#ifndef MYHEADER_H`      |
| `#if`, `#else` | Conditional compilation  | `#if VERSION == 2`        |
| `#elif`    | Else if condition             | `#elif VERSION == 3`      |
| `#endif`   | Ends conditional block        | `#endif`                  |
| `#error`   | Throws compile-time error     | `#error "Wrong version"`  |
| `#pragma`  | Compiler-specific instruction | `#pragma once`            |

---

### 🔹 1. `#include` – Header File Inclusion

Used to include standard or user-defined libraries.

✅ **System Header Files** (angle brackets):
```c
#include <stdio.h>     // Standard I/O
#include <stdlib.h>    // Memory & conversions
#include <math.h>      // Math functions
#include <string.h>    // String functions
#include <ctype.h>     // Character checks
#include <time.h>      // Time/date operations
#include <graphics.h>  // Graphics (platform-specific)
```

#### ✅ User-defined Header Files (double quotes)

```c
#include "myheader.h"
```

### 🔹 2. #define – Macros and Constants
Used to define constant values or macros:

```c
#define PI 3.14159
#define AREA(r) (PI * (r) * (r))
```

📌 Example:
```c
#include <stdio.h>
#define SQUARE(x) ((x)*(x))

int main() {
    int n = 5;
    printf("Square of %d is %d", n, SQUARE(n));
    return 0;
}
```

### 🔹 3. Conditional Compilation
Used to selectively compile code:

```c
#define VERSION 2

#if VERSION == 1
    printf("Version 1 code\n");
#elif VERSION == 2
    printf("Version 2 code\n");
#else
    #error "Unknown version"
#endif
```

### 🔹 4. #ifdef, #ifndef, #endif – Include Guards
Prevents multiple inclusion of the same header:

```c
#ifndef MYHEADER_H
#define MYHEADER_H

// Your header file content

#endif
```

#### ✅ This is called an Include Guard.

### 🔹 5. #pragma – Compiler-Specific Instructions
Used for special instructions to the compiler.

```c

#pragma once                      // Ensures file is included only once
#pragma pack(1)                   // Structure alignment to 1 byte
#pragma warning(disable:4996)     // Suppress specific warning

```
#### 🧠 Extra Facts & Applications of Preprocessor
> ## 🔸 Why Are Preprocessors Important?
>- Help write portable and modular code
>- Improve readability and maintainability
>- Allow platform-specific code
>- Enable conditional compilation for different versions or platforms


> ## 🔸 Real-World Use Cases
✅ Graphics Programming
```c
#include <graphics.h>
```
✅ Mathematical Computation
```c
#include <math.h>
double r = sqrt(25);
```
✅ Game/Simulation Development
```c
#define SCREEN_WIDTH 800
#define SCREEN_HEIGHT 600
```
✅ Logging and Debugging
```c
#define DEBUG
#ifdef DEBUG
    printf("Debug mode is ON\n");
#endif
```
✅ Cross-Platform Compilation
```c
#ifdef _WIN32
    #include <windows.h>
#elif __linux__
    #include <unistd.h>
#endif
```
</details>

---

## 3. **📌 Definition**
   - Uses `#define` preprocessor directive to create constants or macros.
   - Compiler replaces the defined name with its actual value/code.
   - **Example**:
     ```c
     #define long long ll
     ```
---

## 4 **🌐 Global Declaration**
   - Contains:
     - Global variables
     - Function declarations
     - Static variables
   - These are accessible anywhere in the program.

---

## 5. **🔑 Main() Function**
   - Entry point of every C program.
   - All core operations are executed here.
   - **Return types**:
     - `int main()` → returns an integer
     - `void main()` → returns nothing
   - **📌 Example**:
     ```c
     int main() {
         // statements
         return 0;
     }
     ```
---

## 6. **🔧 Sub Programs (User-defined functions)**
   - Functions written by the programmer to perform specific tasks.
   - Called from `main()` or other functions.
   - **📌 Example**:
     ```c
     int sum(int x, int y) {
         return x + y;
     }
     ```

---
---

## **🔹 Character Set in C**

<details>
<summary><strong>Characters used to form words, numbers, expressions:</strong></summary>

- **🔤 Letters** – A-Z, a-z  
- **🔢 Digits** – 0-9  
- **🔣 Special Characters:**:
  - Arithmetic: `+`, `-`, `*`, `/`, `%`
  - Relational: `<`, `>`, `==`, `!=`, `<=`, `>=`
  - Logical: `&&`, `||`, `!`
  - Punctuation: `;`, `:`, `,`, `.`, `?`, `!`
  - Brackets: `()`, `[]`, `{}`
  - Quotes: `'`, `"`
  - Others: `\`, `&`, `$`, `#`

- **⬜ Whitespace Characters**:
  - Space `' '`, Tab `'\t'`, Newline `'\n'`, Carriage return `'\r'`, Form feed `'\f'`
</details>

--
--------------------------------------------------------------------------------------------------------------------------------

## Understanding Format Specifiers in C printf

<details>
<summary><strong>In C, printf is used to display output on the screen. 
It uses format specifiers as placeholders to tell the compiler what type of data you want to print and how to format it.</strong></summary>

## Common Format Specifiers

| **Specifier** | **Data Type**             | **Example Value**    | **Usage**                   |
|-----------|-----------------------|------------------|-------------------------|
| %d        | Integer (int)         | 10, -3, 0        | Prints decimal integer  |
| %c        | Character (char)      | 'A', 'z'         | Prints single character |
| %f        | Floating-point (float/double) | 3.14, 2.0       | Prints float number (decimal) |
| %lf       | Double precision float| 3.14159          | Prints double           |
| %s        | String (char array)   | "Hello"          | Prints string           |
| %u        | Unsigned int          | 10, 100          | Prints unsigned integer |
| %x        | Hexadecimal (int)     | 255              | Prints hex value        |

## How to Replace %d and Use Correct Specifiers
When you write:
```c
printf("Value = %d\n", value);
```

> ** %d means you want to print an integer.
> **value should be an int variable.**
> **At runtime, %d is replaced with the actual integer value of value.**

Example:
```c
int age = 20;
printf("Age is %d\n", age);
```
**Output:**
```c
Age is 20
```

### What happens if you use the wrong specifier?
> If you use %d but pass a float, output will be unpredictable or garbage.
> If you use %f but pass an int, output is undefined behavior.
> Always match the data type with the correct format specifier.

## How to print other types?
Printing a float:
```c
float pi = 3.14159;
printf("Pi = %f\n", pi);
```
> **Output:**
```c
Pi = 3.141590
```

>>**You can control decimal places too:**
```c
printf("Pi = %.2f\n", pi);  // 2 decimal places
```
>> **Output:**
```c
Pi = 3.14
```
Printing a character:
```c
char ch = 'A';
printf("Character is %c\n", ch);
```
**Output:**

```c
Character is A
```

Printing a string:
```c
char name[] = "Urja";
printf("Name is %s\n", name);
```
**Output:**
```c
Name is Urja
```

## **Escaping % in printf**:
Since % is special in printf (used for format specifiers), to print a literal % sign, use %%.
**Example:**
```c
int percent = 85;
printf("You scored %d%% in the test.\n", percent);
```
> **Output:**
```bash
You scored 85% in the test.
```

> ## Summary: How to Replace %d

- %d is replaced by an integer value in the output.

- Use the correct format specifier based on the data type.

- If you want to print % literally, use %%.

</details>

--
--------------------------------------------------------------------------------------------------------------------------------

## 🔹 Keywords and Identifiers

- **⚠️ Keywords**: Reserved words, fixed meaning in C (cannot be used as variable names).  
  Examples: `auto`, `break`, `int`, `float`, `struct`, `union`, `goto`, `for`, `do`, `else`, `switch`

- **🏷️ Identifiers**: Names for variables, functions, arrays, etc.  
  **Rules**:
  - Must start with an alphabet or underscore `_`
  - Can contain letters, digits, underscores
  - Cannot be a keyword
  - No white spaces or commas
  - Only underscore `_` allowed as a special symbol

✅ **Tip**: Use meaningful variable names for better readability.

---

# 🔹 Data Types in C


Divided into:
- **Primary Data Types**
- **Derived Data Types**
- **User-Defined Data Types**

<details>
<summary><strong>🔹 Primary Data Types</strong></summary>

| Type      | Variants                                                                 |
|-----------|--------------------------------------------------------------------------|
| Integer   | `int`, `short int`, `long int`, `unsigned int`, `unsigned short int`, `unsigned long int` |
| Character | `char`, `signed char`, `unsigned char`                                   |
| Float     | `float`, `double`, `long double`                                         |
| Void      | Represents no value                                                      |

### 🔸 Sizes, Ranges, Format Specifiers (32-bit GCC)

| Data Type               | Size (Bytes) | Range                                           | Format |
|------------------------|--------------|--------------------------------------------------|--------|
| short int              | 2            | -32,768 to 32,767                               | %hd    |
| unsigned short int     | 2            | 0 to 65,535                                     | %hu    |
| int                    | 4            | -2,147,483,648 to 2,147,483,647                 | %d     |
| unsigned int           | 4            | 0 to 4,294,967,295                              | %u     |
| long int               | 4            | -2,147,483,648 to 2,147,483,647                 | %ld    |
| unsigned long int      | 4            | 0 to 4,294,967,295                              | %lu    |
| long long int          | 8            | -(2^63) to (2^63)-1                             | %lld   |
| unsigned long long int | 8            | 0 to 18,446,744,073,709,551,615                 | %llu   |
| signed char            | 1            | -128 to 127                                     | %c     |
| unsigned char          | 1            | 0 to 255                                        | %c     |
| float                  | 4            | 1.2E-38 to 3.4E+38                              | %f     |
| double                 | 8            | 1.7E-308 to 1.7E+308                            | %lf    |
| long double            | 16           | 3.4E-4932 to 1.1E+4932                          | %Lf    |

---

### 🔸 Primary Type Declaration

**Syntax**:
```c
datatype var1, var2, ...;
```
📌 Examples:

```c
int count;
double ratio;
```

**🔸 Sample Program: Integer and Float**
```c
#include <stdio.h>

int main() {
    int age = 25;
    float experience = 4.5;

    printf("Age = %d\n", age);
    printf("Total experience = %.1f", experience);

    return 0;
}
```
**Output:**
```
Age = 25
Total experience = 4.5
```
</details>
  
<details>
<summary><strong>🔹 User Defined Data Types</strong></summary>
1. Enum (Enumerated type)
Used for naming integral constants.

**Syntax:**
```c
enum identifier {value1, value2, ..., valueN};
```
📌 Example:
```c
enum day {Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday};
enum day week_st = Monday;
enum day week_end = Friday;
```

## **🔹 Memory Management in C**
A typical memory layout of a C program:

> Text Segment – Stores the compiled machine code (program instructions).

> Initialized Data Segment – Stores global/static variables that are initialized.

> Uninitialized Data Segment (BSS) – Stores global/static variables that are not initialized.

> Heap – Used for dynamic memory allocation during runtime.

> Stack – Stores function calls, local variables, etc.
