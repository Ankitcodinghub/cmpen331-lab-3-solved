# cmpen331-lab-3-solved
**TO GET THIS SOLUTION VISIT:** [CMPEN331 Lab 3 Solved](https://www.ankitcodinghub.com/product/cmpen331-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;123463&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CMPEN331 Lab 3 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
CMPEN 331 – Computer Organization and Design,

Lab 3

This lab introduces the idea of the pipelining technique for building a fast CPU. The students will obtain experience with the design implementation and testing of the first two stages (Instruction Fetch, Instruction Decode) of the five-stage pipelined CPU using the Xilinx design package for FPGAs. It is assumed that students are familiar with the operation of the Xilinx design package for Field Programmable Gate Arrays (FPGAs) through the Xilinix tutorial available in the class website.

1. Pipelining

Pipelining is an implementation technique in which multiple instructions are overlapped in execution. The fivestage pipelined CPU allows overlapping execution of multiple instructions. Although an instruction takes five clock cycle to pass through the pipeline, a new instruction can enter the pipeline during every clock cycle. Under ideal circumstances, the pipelined CPU can produce a result in every clock cycle. Because in a pipelined CPU there are multiple operations in each clock cycle, we must save the temporary results in each pipeline stage into pipeline registers for use in the follow-up stages. We have five stages: IF, ID, EXE, MEM, and WB. The PC can be considered as the first pipeline register at the beginning of the first stage. We name the other pipeline registers as IF/ID, ID/EXE, EXE/MEM, and MEM/WB in sequence. In order to understand in depth how the pipelined CPU works, we will show the circuits that are required in each pipeline stage of a baseline CPU.

2. Circuits of the Instruction Fetch Stage

The circuit in the IF stage are shown in Figure 2. Also, looking at the first clock cycle in Figure 1(b), the first lw instruction is being fetched. In the IF stage, there is an instruction memory module and an adder between two pipeline registers. The left most pipeline register is the PC; it holds 100. In the end of the first cycle (at the rising edge of clk), the instruction fetched from instruction memory is written into the IF/ID register. Meanwhile, the output of the adder (PC + 4, the next PC) is written into PC.

3. Circuits of the Instruction Decode Stage

Referring to Figure 3, in the second cycle, the first instruction entered the ID stage. There are two jobs in the second cycle: to decode the first instruction in the ID stage, and to fetch the second instruction in the IF stage. The two instructions are shown on the top of the figures: the first instruction is in the ID stage, and the second instruction is in the IF stage. The first instruction in the ID stage comes from the IF/ID register. Two operands are read from the register file (Regfile in the figure) based on rs and rt, although the lw instruction does not use the operand in the register rt. The immediate (imm) is sign- extended into 32 bits. The regrt signal is used in the ID stage that selects the destination register number; all others must be written into the ID/EXE register for later use. At the end of the second cycle, all the data and control signals, except for regrt, in the ID stage are written into the ID/EXE register. At the same time, the PC and the IF/ID register are also updated.

Figure 1 Timing chart comparison between two types of CPUs

Figure 2 Pipeline instruction fetch (IF) stage

Figure 3 Pipeline instruction decode (ID) stage

4. Table 1 lists the names and usages of the 32 registers in the register file.

Table 1 MIPS general purpose register

$zero 0 Constant 0

$at 1 Reserved for assembler

$v0, $v1 2, 3 Function return values

$a0 – $a3 4 – 7 Function argument values

$t0 – $t7 8 – 15 Temporary (caller saved)

$s0 – $s7 16 – 23 Temporary (callee saved)

$t8, $t9 24, 25 Temporary (caller saved)

$k0, $k1 26, 27 Reserved for OS Kernel

$gp 28 Pointer to Global Area

$sp 29 Stack Pointer

$fp 30 Frame Pointer

$ra 31 Return Address

5. Table 2 lists some MIPS instructions that will be implemented in our CPU

Table 2 MIPS integration instruction

6. Initialize the first 10 words of the Data memory with the following HEX values:

A00000AA

10000011

20000022

30000033

40000044

50000055

60000066

70000077

80000088

90000099

7. Write a Verilog code that implement the following instructions using the design shown in Figure 2 and Figure 3. Write a Verilog test bench to verify your code: (You have to show all the signals written into the IF/ID register and the ID/EXE register in your simulation outputs)

# address instruction comment

100: lw $v0, 00($at) # $2  memory[$1+00]; load x[0]

104: lw $v1, 04($at) # $3  memory[$1+04]; load x[1]

Assume that the register $at has the value of 0

8. Write a report that contains the following:

a. Your Verilog design code. Use:

i. Device: XC7Z010- CLG400 -1

b. Your Verilog® Test Bench design code. Add “`timescale 1ns/1ps” as the first line of your test bench file.

c. The waveforms resulting from the verification of your design with simulation showing all the signals written into the IF/ID register and the ID/EXE register.

d. The design schematics from the Xilinx synthesis of your design. Do not use any area constraints. e. Snapshot of the I/O Planning and

f. Snapshot of the floor planning

9. REPORT FORMAT: Free form, but it must be:

g. One report per student.

h. Have a cover sheet with identification: Title, Class, Your Name, etc.

i. Using Microsoft word and it should be uploaded in word format not PDF. If you know LaTex, you should upload the Tex file in addition to the PDF file.

j. Double spaced

10. You have to upload the whole project design file zipped with the word file.
