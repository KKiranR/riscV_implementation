## Day4

### Basic RISC-V CPU Micro Architecture

**RISC-V Implementation**

<img width="325" alt="275977401-557382cd-9de9-4d8d-bf53-0ca05e8bfbf7" src="https://github.com/KKiranR/riscV_implementation/assets/89727621/00613eee-ba2d-4b2a-8045-88c2fe9e8c85">

**1.CPU**
The CPU serves as the core of the RISC-V processor, responsible for executing instructions. It includes multiple stages:
- Instruction Fetch(IF):Fetches instructions from memory.
- Instruction Decode (ID): Decodes the fetched instructions.
- Execution (EX): Performs arithmetic and logic operations.
- Memory (MEM): Manages data memory access.
- Write Back (WB): Writes results back to registers.
**2.Program Counter:**
- Program Counter is a register that contains the address of the next instruction to be executed.
- For the initial state, before fetching the first ever instruction, there is a presence of a reset signal that will reset the PC value to 0.
- For branch instructions, we will have immediate instructions, for which we have to add an offset value to the PC. So for branch instructions, ``` NextPC = Incremented PC + Offset value ```

  
  ![Screenshot from 2023-10-18 19-02-51](https://github.com/KKiranR/riscV_implementation/assets/89727621/bd1dee0c-2141-483c-86e4-51f170ee9cf2)

**3.Instruction Fetch:**
- In the Instruction Fetch logic, the instructions are fetched from the instruction memory amd passed to the Decode logic for computation.
- In our case, the Makerchip shell provides us an instantiation to the instruction memory, which contains a test program to compute the sum of numbers from 1 to 9.

  ![Screenshot from 2023-10-18 19-03-31](https://github.com/KKiranR/riscV_implementation/assets/89727621/201fcce4-d64f-4b0a-add6-7651d8a18253)

**4.Decode:**
- Decodes instructions fetched from memory. It translates instructions into actions for the CPU to execute.

![Screenshot from 2023-10-18 19-04-23](https://github.com/KKiranR/riscV_implementation/assets/89727621/23880f19-feab-40ea-843b-43a9c9fca1f1)

- Decode with validity:
 ![Screenshot from 2023-10-18 19-31-00](https://github.com/KKiranR/riscV_implementation/assets/89727621/6a51adc8-e021-4485-aad9-e3fb1294fd62)


  
