Adders (Half Adder & Full Adder) - Theory, Design & Implementation

### Concept Overview
Adders are fundamental arithmetic circuits in digital electronics used for binary addition. There are two primary types of adders: **Half Adder** and **Full Adder**.

### Detailed Explanation

#### ✅ Half Adder
- **Definition:** A half adder is a combinational circuit that adds two single-bit binary numbers and produces a **Sum** and a **Carry** output.
- **Boolean Expressions:**
  - `Sum = A ⊕ B`
  - `Carry = A • B`
- **Truth Table:**

| A | B | Sum | Carry |
|:-:|:-:|:----:|:------:|
| 0 | 0 |  0  |   0   |
| 0 | 1 |  1  |   0   |
| 1 | 0 |  1  |   0   |
| 1 | 1 |  0  |   1   |

**Example Application:** Used in arithmetic logic units (ALUs) and digital counters.

#### ✅ Full Adder
- **Definition:** A full adder is a combinational circuit that adds three single-bit binary numbers: two inputs (`A` and `B`) and one carry-in (`Cin`). It produces a **Sum** and a **Carry-out**.
- **Boolean Expressions:**
  - `Sum = A ⊕ B ⊕ Cin`
  - `Carry = (A • B) + (Cin • (A ⊕ B))`
- **Truth Table:**

| A | B | Cin | Sum | Carry |
|:-:|:-:|:---:|:----:|:------:|
| 0 | 0 |  0  |  0  |   0   |
| 0 | 0 |  1  |  1  |   0   |
| 0 | 1 |  0  |  1  |   0   |
| 0 | 1 |  1  |  0  |   1   |
| 1 | 0 |  0  |  1  |   0   |
| 1 | 0 |  1  |  0  |   1   |
| 1 | 1 |  0  |  0  |   1   |
| 1 | 1 |  1  |  1  |   1   |

**Example Application:** Used in multi-bit binary adders for arithmetic operations.



### Code Explanation
- **`assign` Statements:** Implements XOR and AND logic for the half adder, and XOR-AND-OR logic for the full adder.
- **`$monitor` Task:** Displays real-time changes in inputs and outputs.
- **Test Cases:** Verifies both half adder and full adder logic for various combinations.

### Execution Steps
1. Copy the Verilog code into your simulator (e.g., ModelSim, Xilinx Vivado, etc.).
2. Compile and run the code.
3. Verify that the outputs match the expected truth table values.

### Real-World Example for Practice
- Design a **4-bit Ripple Carry Adder** using multiple full adder modules to add two 4-bit binary numbers.

