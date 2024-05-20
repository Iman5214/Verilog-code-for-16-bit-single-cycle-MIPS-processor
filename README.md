In this project, a 16-bit single-cycle MIPS processor is implemented in Verilog HDL. MIPS is an RISC processor, which is widely used by many universities in academic courses related to computer organization and architecture. 
Below is the description for instructions being implemented in Verilog:

Add : R[rd] = R[rs] + R[rt]
Subtract : R[rd] = R[rs] - R[rt]
And: R[rd] = R[rs] & R[rt]
Or : R[rd] = R[rs] | R[rt]
SLT: R[rd] = 1 if R[rs] <  R[rt] else 0
Jr: PC=R[rs]
Lw: R[rt] = M[R[rs]+SignExtImm]
Sw : M[R[rs]+SignExtImm] = R[rt]
Beq : if(R[rs]==R[rt]) PC=PC+1+BranchAddr
Addi: R[rt] = R[rs] + SignExtImm
J :  PC=JumpAddr
Jal : R[7]=PC+2;PC=JumpAddr
SLTI: R[rt] = 1 if R[rs] < imm else 0
 SignExtImm = { 9{immediate[6]}, imm
JumpAddr =    { (PC+1)[15:13], address}
                BranchAddr = { 7{immediate[6]}, immediate, 1’b0 }
Based on the provided instruction set, the data-path and control unit are designed and implemented.
