## 🛠️ Requirements & Installation

This project builds and runs on both **Linux** and **Windows (via MSYS2)**.

---

### ✅ Linux Setup (Ubuntu / Debian-based)

Install the required tools:

```bash
sudo apt update
sudo apt install build-essential gdb make
```

> `build-essential` includes `gcc`, `g++`, and `make`.

---

### ✅ Windows Setup (MSYS2)

1. **Download and install MSYS2**
   👉 [https://www.msys2.org/](https://www.msys2.org/)

2. Open the **MSYS2 MinGW 64-bit** terminal (not the plain MSYS2 shell).

3. Update and install the required packages:

```bash
pacman -Syu
pacman -S mingw-w64-x86_64-gcc mingw-w64-x86_64-gdb make
```

> If prompted to restart the shell, close and reopen **MSYS2 MinGW 64-bit** before running the second `pacman` command.

4. Set up **VS Code** to use MSYS2:

   * Open **Command Palette** → `Terminal: Select Default Profile` → select `MSYS2 MinGW 64-bit`
   * In `.vscode/launch.json`, ensure the Windows debugger path is:

```json
"miDebuggerPath": "C:/msys64/mingw64/bin/gdb.exe"
```

---

### ✅ Recommended VS Code Extensions

Install these from the **VS Code Marketplace**:

* [C/C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools) (by Microsoft) — IntelliSense and debugger
* [Makefile Tools](https://marketplace.visualstudio.com/items?itemName=ms-vscode.makefile-tools) (optional but helpful)

---

## 🧪 Building the Project

From the terminal or using the VS Code build task:

```bash
make        # Build the project
make run    # Build and run the program
make clean  # Clean build artifacts
```

---

## 🧾 Running and Debugging

In VS Code:

1. Press `F5` or go to **Run → Start Debugging**
2. Choose the correct debug config:

   * `Debug my_c_program (Linux)`
   * `Debug my_c_program (Windows)`

---

### ✅ Expected Output

When successful, the program will print:

```
Hello, cross-platform world!
```
