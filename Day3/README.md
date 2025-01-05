# Day 3: Combinational and Sequential Optimizations

## 1. Combinational Logic optimizations

**To synthesize an optimal combinational logic following code block has been used:**
```
yosys>read_liberty -lib {sky130_standard_cell_library.lib}
yosys>read_verilog {design_file.v}
yosys>synth -top {module_name}
yosys>flatten
yosys>opt_clean -purge
yosys>abc -liberty {sky130_standard_cell_library.lib}
yosys>show
```
### 1.1 Synthesized combinational logic blocks

#### 1.1.1 opt_check

![opt_check](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day3/assets/comb_logic_opt/synth_opt_check.png)

#### 1.1.2 opt_check2

![opt_check2](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day3/assets/comb_logic_opt/synth_opt_check2.png)

#### 1.1.3 opt_check3

![opt_check3](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day3/assets/comb_logic_opt/synth_opt_check3.png)

#### 1.1.4 opt_check4

![opt_check4](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day3/assets/comb_logic_opt/synth_opt_check4.png)

#### 1.1.5 multiple_module_opt

![multiple_module_opt](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day3/assets/comb_logic_opt/synth_multiple_module_opt.png)

#### 1.1.6 multiple_module_opt2

![multiple_module_opt2](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day3/assets/comb_logic_opt/synth_multiple_module_opt2.png)

## 2. Sequential Logic optimizations 

### 2.1 Functional Verification and Synthesis of Sequential Circuit Elements

#### 2.1.1 dff_const1

**Functional Verification:**

![dff_const1_fv]()

**Synthesized Design:**

![dff_const1_synth]()

#### 2.1.2 dff_const2

**Functional Verification:**

![dff_const2_fv]()

**Synthesized Design:**

![dff_const2_synth]()

#### 2.1.3 dff_const3

**Functional Verification:**

![dff_const3_fv]()

**Synthesized Design:**

![dff_const3_synth]()

#### 2.1.4 dff_const4

**Functional Verification:**

![dff_const4_fv]()

**Synthesized Design:**

![dff_const4_synth]()

#### 2.1.5 dff_const5

**Functional Verification:**

![dff_const5_fv]()

**Synthesized Design:**

![dff_const5_synth]()

#### 2.1.6 counter_opt

**Synthesized Design:**

![counter_opt_synth]()

#### 2.1.7 counter_opt2

**Synthesized Design:**

![counter_opt2_synth]()

 
