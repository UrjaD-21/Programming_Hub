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
