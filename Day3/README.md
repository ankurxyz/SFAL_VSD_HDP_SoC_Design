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

![]()

#### 1.1.2 opt_check2

![]()

#### 1.1.3 opt_check3

![]()

#### 1.1.4 opt_check4

![]()

#### 1.1.5 multiple_module_opt

![]()

#### 1.1.6 multiple_module_opt2

![]()

## 2. Sequential Logic optimizations  
