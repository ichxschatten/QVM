# QVM - Simple Assembler and Virtual Machine

QVM is a minimalistic assembler and virtual machine for educational and demonstration purposes.  
It reads an assembly-like program from a text file, assembles it into machine code, and executes it.

---

## Features

- **Assembler**: Converts human-readable assembly code into machine code.
- **Virtual Machine**: Executes the assembled code with support for arithmetic, memory, and control flow.
- **Labels and Directives**: Supports labels, data, and memory reservation.
- **Simple Syntax**: Easy to read and write assembly programs.

---

## File Structure

- `QVM.exe` — The executable for the assembler and virtual machine.
- `awakening.qvm` — Example assembly program (see below).

---

## Usage

1. **Write your assembly program** in a file named `awakening.qvm` (see example below).
2. **Place `QVM.exe` and `awakening.qvm` in the same directory.**
3. **Run the virtual machine:**

   ```
   QVM.exe
   ```

4. The program will assemble and execute your code, printing the result if a `RESULT` label is present.

---

## Assembly Language Reference

- **Labels**: `LABEL:`
- **Instructions**:  
  `LD`, `STO`, `ADD`, `SUB`, `MUL`, `DIV`, `JUMP`, `JGE`, `JNE`, `HALT`
- **Directives**:
    - `ORG <address>` — Set the origin address for code or data.
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

## Output Example

```
Execution completed. Result: 30
```

---

## Custom Programs

- Write your own program in the same format.
- Save it as `awakening.qvm` or change the filename in the executable if needed.

---

## License

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---
