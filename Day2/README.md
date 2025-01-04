# Day 2:
## Hierarchical Design Synthesis

In Hierarchical design synthesis, the sub module synthesis is not visible in the synthesized design.

**Step1:** Read sky130 standard cell library

![read_library](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day2/assets/hierarchical_netlist/1_read_library.png)

**Step2:** Read RTL Design file

![read_rtl](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day2/assets/hierarchical_netlist/2_read_verilog.png)

**Step3:** Synthesized Design 

![synthesized_design](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day2/assets/hierarchical_netlist/3_synthesized_design.png)

**Step4:** Linking Synthesized design to sky130 standard cell library

![linking](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day2/assets/hierarchical_netlist/4_design_linking.png)

**Step5:** Using show command to visualize the synthesized design

![show](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day2/assets/hierarchical_netlist/5_show_cmd.png)

**Step6:** View Synthesized Design

![view_synth](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day2/assets/hierarchical_netlist/6_view_synth_design.png)

**Step7:** Write netlist

![write_netlist](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day2/assets/hierarchical_netlist/7_write_gate_netlist.png)

**Step8:** Hierarchical netlist

![hierarchical_netlist](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day2/assets/hierarchical_netlist/8_hierarchical_netlist.png)

## Flattened Design Synthesis

In Flattened Design Synthesis, the whole design is synthesized in one single module.
For flattened design synthesis, after linking design to standard cell library run the below command

![flat](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day2/assets/flatten_netlist/1_flatten_synth_design.png)

The synthesized design is flattened as shown in the below image

![view_synth_design](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day2/assets/flatten_netlist/2_view_synth_design.png)

and has the following gate level netlist

![flat_netlist](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day2/assets/flatten_netlist/3_flat_netlist.png)

## Sub-Module Level Synthesis

It is done when the design is very large or the synthesis tool has some limitation in handling large designs. In this methodology, different kinds of module that are used in design are synthesized separately and then replicated for their various instances.

Use below command to synthesize sub_module1

![sub_module_synth](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day2/assets/submodule_level_synth/1_sub_module_synth.png)

The below image shows the synthesized sub_module1

![view_synth_design](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day2/assets/submodule_level_synth/2_view_synth_design.png)

## Functional Verification and Synthesis of Sequential Circuit Elements

### Code for Functional Verification of design
`
**$**iverilog {design_file.v} {test_bench_file.v}
**$**./a.out
**$**gtkwave {vcd_file.vcd}
`

### Code for Design Synthesis
`
**yosys>**read_liberty -lib {standard_cell_library_file}
**yosys>**read_verilog {design_file.v}
**yosys>**synth -top {module_name}
**yosys>**dfflibmap -liberty {dff_standard_cell_library_file}
**yosys>**abc -liberty {standard_cell_library_file}
**yosys>**show
`

**1. D Flip Flop with asynchronous reset:**
 
Functional Simulation waveform:

![dff_asyncres_func_sim]()

Synthesized Design:

![dff_asyncres_synth]()

**2. D Flip Flop with asynchronous set:**

Functional Simulation waveform:

![dff_asyncset_func_sim]()

Synthesized Design:

![dff_asyncset_synth]()

**3. D Flip Flop with synchronous reset:**

Functional Simulation waveform:

![dff_syncres_func_sim]()

Synthesized Design:

![dff_syncres_synth]()

## Multiplier Design Synthesis:

**1. Mult2(out = in x 2) Synthesis:**

![mul2_synth]()

**2. Mult8(out = in x 8) Synthesis:**

![mul8_synth]()




   