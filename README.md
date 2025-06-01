# QVM (Q Virtual Machine) - Simple Assembler and Virtual Machine

This project is a simple assembler and virtual machine written in Go.  
It reads an assembly-like program from a text file, assembles it into machine code, and executes it in a virtual machine.

---

## Features

- **Assembler**: Converts human-readable assembly code into machine code.
- **Virtual Machine**: Executes the assembled machine code.
- **Labels and Directives**: Supports labels, data, and memory reservation directives.
- **Simple Arithmetic and Control Flow**: Supports basic arithmetic and jump instructions.

---

## File Structure

- `QVM.go` — Main source code for the assembler and virtual machine.
- `awakening.qvm` — Example assembly program (see below).

---

## How It Works

1. **Write your assembly program** in a `.qvm` file (see example below).
2. **Run the program**. It will:
    - Read and assemble the `.qvm` file.
    - Execute the resulting machine code.
    - Print the result (if a `RESULT` label is present).

---

## Assembly Language Syntax

- **Labels**: `LABEL:`
- **Instructions**: `LD`, `STO`, `ADD`, `SUB`, `MUL`, `DIV`, `JUMP`, `JGE`, `JNE`, `HALT`
- **Directives**:
    - `ORG <address>` — Set program/data origin.
    - `DATA <value>` — Define a data value.
    - `BSS <size>` — Reserve uninitialized memory.
    - `END` — End of program.

---

## Example Program (`awakening.qvm`)

```
        ORG 0
START:  LD A
        ADD B
        MUL TWO
        STO RESULT
        HALT

        ORG 20
A:      DATA 10
B:      DATA 5
TWO:    DATA 2
RESULT: BSS 1
        END
```

This program calculates `(A + B) * TWO` and stores the result in `RESULT`.

---

## How to Run

1. **Clone this repository** or copy the files to a directory.
2. Place your assembly program in a file named `awakening.qvm` in the same directory.
3. Open a terminal and run:

   ```
   ./QVM.exe
   ```

5. **Output**:  
   If the program contains a label `RESULT`, its value will be printed after execution.

---

## Output Example

```
Execution completed. Result: 30
```

---

## Adding Your Own Programs

- Write your program in the same assembly format as above.
- Save it as `awakening.qvm`.

---

## License

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## Author

ICHxSchatten

---
