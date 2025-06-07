# 🚀 Getting Started with C Programming using VS Code + MinGW (Windows)

Welcome to your C programming journey! 🧠💡  
This guide will walk you step-by-step through setting up your development environment using **Visual Studio Code** and **MinGW** (C Compiler) on Windows.

---

## 🛠️ Tools You’ll Need

| Tool         | Purpose                 | Download Link                                  |
|--------------|--------------------------|------------------------------------------------|
| VS Code      | Code editor              | [🔗 Download](https://code.visualstudio.com/)  |
| MinGW        | C Compiler for Windows   | [🔗 Download](https://sourceforge.net/projects/mingw/) |

---

## 🧩 Step-by-Step Setup Guide

### 🖥️ 1. Install **VS Code**

1. Download from [Visual Studio Code](https://code.visualstudio.com/)
2. Run the installer.
3. During installation, ✅ check:
   - `Add to PATH`
   - `Add "Open with Code"`

📌 This lets you open folders directly in VS Code.

---

### ⚙️ 2. Install **MinGW (C Compiler)**

1. Download from [MinGW SourceForge](https://sourceforge.net/projects/mingw/)
2. Run the `mingw-get-setup.exe` installer
3. Select these packages for installation:
   - `mingw32-gcc-g++`
   - `mingw32-base`
4. Go to `Installation > Apply Changes`
---

### 🧭 3. Add MinGW to **System PATH**

🔹 Locate MinGW’s bin path:  
`C:\MinGW\bin`

📌 Then follow these steps:
- Search **“Environment Variables”** in Start menu
- Under **System Variables**, find `Path` → Edit → New
- Paste: `C:\MinGW\bin`
- Save and close all windows

✅ To verify:
Open Command Prompt and type:
```bash
gcc --version
```

### 🍎 For macOS

1. Open Terminal  
2. Install Xcode Command Line Tools:

    ```bash
    xcode-select --install
    ```

3. Verify:

    ```bash
    gcc --version
    ```

---

### 🐧 For Linux (Ubuntu/Debian)

1. Open Terminal  
2. Install GCC using:

    ```bash
    sudo apt update
    sudo apt install build-essential
    ```

3. Check:

    ```bash
    gcc --version
    ```

---

### ✍️ Step 3: Create Your First C Program

1. Open VS Code  
2. Create a new file named `hello.c`  
3. Paste this code:

    ```c
    #include <stdio.h>

    int main() {
        printf("Hello World!\\n");
        return 0;
    }
    ```

---

### 🚀 Step 4: Compile & Run `hello.c`

---

#### 🪟 Windows Steps

1. Open **Command Prompt** or **terminal** in VS Code  
2. Navigate to the folder where `hello.c` is saved  
3. Compile using:

    ```bash
    gcc hello.c -o hello.exe
    ```

4. Run it:

    ```bash
    ./hello.exe
    ```

✅ You should see:

Hello World!
---

#### 🍎 macOS Steps

1. Open **Terminal**  
2. Navigate to the folder where `hello.c` is saved  
3. Compile using:

    ```bash
    gcc hello.c -o hello
    ```

4. Run it:

    ```bash
    ./hello
    ```

✅ You should see:

Hello World!
---

#### 🐧 Linux Steps

1. Open **Terminal**  
2. Navigate to the folder where `hello.c` is saved  
3. Compile using:

    ```bash
    gcc hello.c -o hello
    ```

4. Run it:

    ```bash
    ./hello
    ```

✅ You should see:
Hello World!
---

### 🧩 Common Errors & Solutions

| Issue                                  | Solution                                                             |
|---------------------------------------|----------------------------------------------------------------------|
| `'gcc' is not recognized` (Windows)   | Make sure `C:\MinGW\bin` is correctly added to the **Path** variable |
| `Permission denied` (Linux/macOS)     | Run `chmod +x hello` to make it executable before running            |
| `File not found`                      | Check that you're in the correct folder and the filename is correct  |
| `Output not printing`                 | Ensure `printf()` statement is correct and saved properly            |
