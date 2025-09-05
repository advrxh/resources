# **Computer Architecture & Data Representation**

## **1. Binary Representation of Data and Numbers**

### **1.1 Binary Number System**
- The **binary number system** is a **base-2** system, meaning it uses only two digits: `0` and `1`.
- Every number in a computer is represented in **binary** because computers use **electrical signals** (on/off).
- Example:
  - Decimal `5` in binary:  
    ```
    5 (Decimal) = 101 (Binary)
    ```

### **1.2 Binary to Decimal Conversion**
Convert binary `1010` to decimal:
```
(1 × 2³) + (0 × 2²) + (1 × 2¹) + (0 × 2⁰)
= 8 + 0 + 2 + 0
= 10 (Decimal)
```

### **1.3 Decimal to Binary Conversion**
Convert decimal `13` to binary:
1. Divide by 2 and write the remainder.
2. Read from bottom to top.

```
13 ÷ 2 = 6 remainder 1
6 ÷ 2  = 3 remainder 0
3 ÷ 2  = 1 remainder 1
1 ÷ 2  = 0 remainder 1
```
**Binary: `1101`**

## **2. Integer Representation**
Numbers in computers can be represented in different ways.

### **2.1 Unsigned Integers (Only Positive Numbers)**
- Example (8-bit representation):  
  ```
  00001100 = 12 (Decimal)
  ```

### **2.2 Signed Integers (Using Two's Complement)**
- Two’s complement is used to represent negative numbers.
- **Example: -12 in 8-bit Two’s Complement**:
  1. Write `12` in binary: `00001100`
  2. Take one’s complement: `11110011`
  3. Add `1`: `11110100`
  - Final **two’s complement representation** of `-12` is:  
    ```
    11110100
    ```

## **3. Data Storage Units**
Data is stored in **bits and bytes**, measured in different units.

| Unit        | Size (Bytes) | Equivalent |
|------------|------------|------------|
| **Bit**    | -          | Smallest unit (0 or 1) |
| **Nibble** | ½ byte     | 4 bits |
| **Byte**   | 1          | 8 bits |
| **Kilobyte (KB)** | 1,024 bytes | ~1,000 bytes |
| **Megabyte (MB)** | 1,024 KB | ~1 million bytes |
| **Gigabyte (GB)** | 1,024 MB | ~1 billion bytes |
| **Terabyte (TB)** | 1,024 GB | ~1 trillion bytes |

## **4. ASCII and Unicode**
### **4.1 ASCII (American Standard Code for Information Interchange)**
- A **7-bit character encoding** system (0–127 unique characters).
- Example:
  ```
  'A' = 65 (Binary: 1000001)
  'a' = 97 (Binary: 1100001)
  '0' = 48 (Binary: 0110000)
  ```

### **4.2 Unicode**
- Unicode supports **multiple languages** and symbols, unlike ASCII.
- Uses **UTF-8, UTF-16, and UTF-32** encoding schemes.
- Example:
  ```
  'A' in Unicode (UTF-8) = U+0041
  '😊' in Unicode = U+1F60A
  ```

## **5. CPU Architecture and Instruction Set**

### **5.1 Basic CPU Architecture**
The CPU consists of three main parts:

```
  +-----------------------+
  |   Control Unit (CU)   |  <-- Directs operations
  +-----------------------+
  |   Arithmetic Logic    |  <-- Performs calculations
  |      Unit (ALU)       |
  +-----------------------+
  |      Registers        |  <-- Stores temporary data
  +-----------------------+
```

1. **Control Unit (CU):** Directs instruction execution.
2. **Arithmetic Logic Unit (ALU):** Performs mathematical operations.
3. **Registers:** Small, fast storage for immediate values.

## **6. Instruction Format & Assembly Language**
### **6.1 Instruction Format**
Instructions consist of:
```
[Opcode] [Operand]
```
- **Opcode:** Specifies the operation (e.g., ADD, SUB, MOV).
- **Operand:** Specifies data or memory location.

### **6.2 Example Assembly Language Instructions**
```assembly
MOV AX, 5  ; Move value 5 into register AX
ADD AX, 3  ; Add 3 to AX
SUB AX, 2  ; Subtract 2 from AX
```

## **7. Fetch-Execute Cycle**
The CPU follows a cycle to execute instructions.

### **7.1 Fetch-Execute Cycle Steps**
1. **Fetch**: The CPU fetches the instruction from memory.
2. **Decode**: The Control Unit interprets the instruction.
3. **Execute**: The ALU performs the operation.
4. **Store**: The result is stored in a register or memory.

### **7.2 Fetch-Execute Cycle Flowchart**
```
    +-------------------+
    | Fetch Instruction |
    +-------------------+
             ↓
    +--------------------+
    | Decode Instruction |
    +--------------------+
             ↓
    +-------------------+
    | Execute Operation |
    +-------------------+
             ↓
    +-----------------+
    | Store Result    |
    +-----------------+
             ↓
    +-----------------+
    | Next Instruction|
    +-----------------+
```

## **Final Thoughts**
- **Binary is the foundation** of all data representation.
- **Two’s complement** is used for signed numbers.
- **ASCII and Unicode** define character encoding.
- **CPU architecture** consists of the ALU, CU, and registers.
- **The Fetch-Execute Cycle** governs instruction execution.

Understanding these concepts is **key to mastering computer architecture and low-level computing**. 🚀

