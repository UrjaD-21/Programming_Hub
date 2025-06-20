# 📘 Chapter 2: Control Flow

_🔹 What is **Control Flow**?_
> **Control flow** refers to _the order_ in which individual statements, instructions, or function calls are executed in a program. By default, code _**is executed sequentially**_ — line by line — but control flow allows decision-making and repetition.

--

## **1️⃣ Conditional Statements (Decision Making)**
- These allow programs _**to choose different paths based on conditions**_.

### **✅ if Statement**
> - _**🔍 Checks a condition**_
> - 🟢 Executes a block of code only **if the condition is true**.

> **Syntax (C/C++):**
> ```c
>   if (condition) {
>   // Code to execute if condition is true
>   }
> ```

> **Example:**
> ```c
>   int age = 18;
>   if (age >= 18) {
>      printf("You are eligible to vote.");
>   }
> ```

### **🔁 if...else Statement**
> - _**🔍 Checks a condition**_
> - ➡️ 🟢 If true: executes one block
> - ➡️ 🔴 If false: executes another block
> - 🟢 Executes one block if the condition is true, another if false.

> **Syntax:**
> ```c
> if (condition) {
>   // Executes if condition is true
> } else {
>   // Executes if condition is false
> }
> ```

> **Example:**
> ```c
> int number = 5;
> if (number % 2 == 0) {
>   printf("Even");
> } else {
>   printf("Odd");
> }
> ```

### **🪜 else if Ladder**
> - 📚 **Checks multiple conditions** _one by one_
> - 🔄 Used when you have multiple conditions to test.

> **Syntax:**
> ```c
> if (condition1) {
>    // Executes if condition1 is true
> } else if (condition2) {
>     // Executes if condition2 is true
> } else {
>    // Executes if none are true
> }
> ```

> **Example:**
> ```c
> int marks = 85;
> if (marks >= 90) {
>    printf("Grade A");
> } else if (marks >= 75) {
>    printf("Grade B");
> } else {
>     printf("Grade C");
> }
> ```

### **✅ d. switch Statement**
> - 🔢 Best when testing a single variable against multiple values
> - 📖 ✅ More readable than using many `else if` statements

> **Syntax:**
> ```c
> switch (expression) {
>    case value1:
>        // Code
>        break;
>    case value2:
>        // Code
>        break;
>    default:
>        // Code
> }
> ```

> **Example:**
> ```c
> int day = 3;
> switch (day) {
>    case 1: printf("Monday"); break;
>    case 2: printf("Tuesday"); break;
>    case 3: printf("Wednesday"); break;
>    default: printf("Invalid");
> }
> ```
>  

## **2️⃣ Loops (Iteration)**
- Loops let you **repeat code multiple times** based on conditions.

### **🔁 a. for Loop**
> Used when the number of iterations is known.
> **Syntax:**
> ```c
> for (initialization; condition; increment) {
>     // Code block
> }
> ```
> **Example:**
> ```c
> for (int i = 1; i <= 5; i++) {
>     printf("%d ", i);
> }
> ```

### **🔁 b. while Loop**
> Used when the **number of iterations** is **not known in advance**.

> **Syntax:**
> ```c
> while (condition) {
>     // Code block
> }
> ```

> **Example:**
> ```c
> int i = 1;
> while (i <= 5) {
>     printf("%d ", i);
>     i++;
> }
> ```

### **🔁 c. do...while Loop**
> **Runs at least once** even if the condition is false (because condition is checked after running the loop).

> **Syntax:**
> ```c
> do {
>     // Code block
> } while (condition);
> ```

> **Example:**
> ```c
> int i = 1;
> do {
>     printf("%d ", i);
>     i++;
> } while (i <= 5);
> ```

### **3️⃣ Loop Control Statements**
> Used to **alter normal loop execution**.

#### **🔸 a. break**
> - Terminates the loop immediately and moves control to the next statement after the loop.

> _**Example:**_
> ```c
>   for (int i = 1; i <= 5; i++) {
>      if (i == 3) break;
>      printf("%d ", i);
>      }
> ```

#### **🔸 b. continue**
> - Skips the current iteration and continues with the next one.

> _**Example:**_
> ```c
> for (int i = 1; i <= 5; i++) {
>     if (i == 3) continue;
>     printf("%d ", i);
> }
> // Output: 1 2 4 5
> ```


### **4️⃣ Nested Control Flow**
> You can combine loops and conditionals inside each other.

> **Example:** Nested `for` Loop
> ```c
> for (int i = 1; i <= 3; i++) {
>     for (int j = 1; j <= 2; j++) {
>         printf("i=%d j=%d\n", i, j);
>     }
> }
> ```

---

## **🧠 Important Notes :**
| _Keyword_    | _Meaning_                                           |
| ---------- | ------------------------------------------------- |
| `if`       | Runs block if condition is true                   |
| `else`     | Runs block if condition is false                  |
| `switch`   | Multi-way branching based on variable             |
| `for`      | Loop with known iteration count                   |
| `while`    | Loop with unknown count, condition-checked first  |
| `do-while` | Loop that runs once before checking the condition |
| `break`    | Exits loop or switch immediately                  |
| `continue` | Skips to next loop iteration                      |


# 🧪 Sample Practice Questions
