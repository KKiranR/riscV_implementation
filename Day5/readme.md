## DAY 5
### Pipelining the cpu

**Introduction to Control FLow and Read After Write Hazard**
**1.Waterfall diagram:**

<img width="446" alt="276124489-8354dd73-716c-4054-980b-1c75b1457bd4" src="https://github.com/KKiranR/riscV_implementation/assets/89727621/2840e3d7-b980-4281-be75-52fb9dceaba5">

**2.Control flow Hazard:**

- Control flow hazards, also known as control hazards, occur when the normal sequential flow of instructions is disrupted due to conditional branch instructions.
- These hazards can lead to incorrect program execution and reduced performance.
- There are three main types of control flow hazards: * Branch Hazards: These occur when a branch instruction (e.g., a conditional jump) is encountered, and the processor is unsure about the branch target. The processor may need to stall the pipeline or make speculative predictions to mitigate the impact of these hazards. * Jump Hazards: Jump instructions that cause a change in the program counter can also create hazards, as they affect the instruction fetch stage and can lead to pipeline bubbles (stalls). * Return Hazards: Similar to jump hazards, but related to function calls and returns. These can disrupt the flow of instructions.

**3.Read After Write Hazard:**

- Read-after-write hazards, often referred to as data hazards, occur when an instruction depends on the result of a previous instruction that has not yet completed.
- There are three main types of read-after-write hazards: * True Data Dependency: This occurs when an instruction (e.g., a load or ALU operation) depends on the result of a previous instruction. The hazard arises because the dependent instruction cannot proceed until the producing instruction has written its result. 
- **Anti-Data Dependency:** This occurs when a previous instruction depends on a result produced by a later instruction. This situation can cause issues when instructions are executed out of order.
- ** Output Data Dependency (Write-After-Read): **This happens when two instructions need to read from the same register, and the second instruction wants to read before the first instruction writes to the register. This can lead to incorrect results if not managed properly.

## LABS
1.Lab to create 3-cycle valid signal:
  
  ![image](https://github.com/KKiranR/riscV_implementation/assets/89727621/0cc288f7-cacb-4866-a638-f62e260181c7)
2.Modify 3 cycle to distribute logic:

![image](https://github.com/KKiranR/riscV_implementation/assets/89727621/191f3e32-df67-4767-b941-8f2802ff8516)

3.Instruction Decode:

![image](https://github.com/KKiranR/riscV_implementation/assets/89727621/27abb919-e417-4e88-b18f-108e8c2ea6f7)

4.Complete ALU:

![image](https://github.com/KKiranR/riscV_implementation/assets/89727621/495c5bfe-5854-487c-8be5-9eb72c35c449)

### Load/Store Instructions and Completing RISC-V CPU

1.Lab to redirect loads:

![image](https://github.com/KKiranR/riscV_implementation/assets/89727621/564a7125-4e8b-4dde-98fb-06282dfc666b)

2.Lab to Data From Memory to Register File:

![image](https://github.com/KKiranR/riscV_implementation/assets/89727621/0f3cb855-2bef-4e5a-b5dd-7801a61e167f)

3.Lab to Instantiate Data Memory to CPU:

![image](https://github.com/KKiranR/riscV_implementation/assets/89727621/78a3bd6a-bbdc-467d-8445-2dc0385ef563)

4.Lab for Jump Instructions:

![image](https://github.com/KKiranR/riscV_implementation/assets/89727621/04174e36-0a3d-4edf-8ec9-6053d0a414a8)


### Final RISC-V Core
![image](https://github.com/KKiranR/riscV_implementation/assets/89727621/df54af87-7c9e-429d-a7ff-0eb19d73b149)
