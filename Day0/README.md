# Day 0
## Task 1: Summary of Task 0

### Steps involved in the development of a chip:

**Step1:** Create a software application in C programming language, compile it using the gcc compiler and execute it. After execution measure the output O0.

**Step2:** Run the same application in a C kind of an environment where specifications of the hardware are given as to whether the hardware is made on RISCV-ISA or ARM-ISA or x86-ISA etc. Measure output O1. The goal here is to ensure that O0 = O1.

**Step3:** IP Design<br />
Describe the digital circuit/hardware using HDL such as Verilog/VHDL or Bluespec or Chisel. Run the same application on DUT and measure the output O2. The goal here is to ensure that O1 = O2.
In this step, using RTL code we create synthesizable IP of Processor and Macros while Analog IP's such as PLL and ADC are defined at the transistor level.

**Step4:** IP Integration/SoC Design\
Here the SoC Designer integrate the IP's using GPIO's.

**Step5:** Physical Design<br />
The step involves Floorplanning, Placement, Clock Tree Synthesis and Routing.

**Step6:** Physical Verification of GDSII file using DRC and LVS leading to the TAPEOUT.

**Step7:** Chip Fabrication by the foundry(usually takes 4 to 6 months) taking the GDSII file into account.

**Step8:** TAPEIN

**Step9:** The embedded chip on board is then further tested by driving signals from the peripherals on board and measuring output O4 at the output pin. The goal here is to ensure that O1 = O2 = O3 = O4.

### Terminology:
1. **Macros:** IP blocks that can be instantiated.
2. **TAPEOUT:** The process of sending the GDSII file to the Fab post Physical Verification.
3. **TAPEIN:** The process of receiving packaged chips back from the fab.

### Acronyms:
1. **GDSII:** Graphic Datastream Information Interchange

## Task 2: Tool Installation Snippet

### 1. Ubuntu 22.04 LTS

![ubuntu](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/images/Ubuntu%2020.04%20LTS.png)

### 2. Yosys

![yosys](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/images/Yosys.png)

### 3. Iverilog

![iverilog](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/images/iverilog.png)

### 4. gtkwave

![gtkwave](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/images/gtkwave.png)

### 5. OpenSTA

![opensta](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/images/OpenSTA.png)

### 6. ngspice

![ngspice](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/images/ngspice.png)

### 7. magic

![magic](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/images/magic.png)

### 8. OpenLane

![openlane](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/images/OpenLane.png)
