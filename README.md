# Nand2Tetris Project 5: CPU Implementation

This repository contains the implementation of the **CPU.hdl** file for **Project 5** of the [Nand2Tetris course](https://www.nand2tetris.org/). The objective of this project is to build the central processing unit (CPU) of the Hack computer, as described in Chapter 5 of the course.

---

## Project Overview

The Hack CPU is the core component of the Hack computer, responsible for executing instructions according to the Hack machine language. It integrates the **ALU**, **registers**, and logic for fetching and executing instructions, supporting the `C`-type (computation) and `A`-type (addressing) commands.

The CPU module:
- Executes arithmetic and logical operations using the ALU.
- Handles control logic for jumping to specific instructions based on the current computation.
- Stores data in the **A register** and the **D register**.
- Outputs the address of the next instruction to fetch.

---

## Components

The CPU is composed of:
1. **Arithmetic Logic Unit (ALU)**: Executes the desired computation.
2. **Registers**:
   - **A Register**: Stores addresses or constants.
   - **D Register**: Holds data for computations.
3. **Control Logic**:
   - Determines when to jump based on conditions.
   - Decides how to load values into the registers.

---

## Key Features

1. **Instruction Parsing**:
   - Differentiates between `A-instructions` and `C-instructions`.
   - Extracts control bits (`dest`, `comp`, `jump`) from `C-instructions`.

2. **Jump Logic**:
   - Implements conditional branching by evaluating the ALU's output (`zr` and `ng` flags).

3. **Memory Interaction**:
   - Outputs the current memory address (`outM`).
   - Reads and writes data from/to memory (`writeM`).

4. **Data Flow**:
   - Routes data between the ALU, registers, and memory.

---

## File Structure

- **CPU.hdl**: The hardware description language file for the CPU implementation.
- **CPU.tst**: The test script used to verify the functionality of the CPU.
- **CPU.cmp**: The expected output of the test script.
- **README.md**: This documentation file.

---

## Testing

1. Open the **Hardware Simulator** provided with the Nand2Tetris tools.
2. Load the `CPU.tst` script into the simulator.
3. Run the script to verify the CPU's implementation.
4. Compare the output with the `CPU.cmp` file to ensure correctness.

---

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/nand2tetris-project5.git
   cd nand2tetris-project5
   ```

2. Open **CPU.hdl** in the Hardware Simulator.
3. Test using the provided test scripts.

---

## Example Instruction Execution

- **Instruction**: `D=D+M;JGT`
  - ALU computes `D + M`.
  - Stores the result in the `D` register.
  - If the result is greater than 0, the program counter (PC) jumps to the specified address.

---

## Resources

- [Nand2Tetris Official Website](https://www.nand2tetris.org/)
- [Project 5 Specification](https://www.nand2tetris.org/project05)

---

## Author

This implementation was completed as part of the **Nand2Tetris course**, which is a hands-on journey through building a computer from the ground up.

Feel free to contribute or report issues! 😊

--- 

## License

This project is licensed under the MIT License.
