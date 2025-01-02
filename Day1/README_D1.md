# Day 1
## Functional Verification and Synthesis of 2x1 MUX

### Steps:

**Step1:** Passing RTL Design and correspodning testbench as input to the iverilog simulator

![design_tb_inp_to_simulator](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day1/images_mux_2x1/functional_verification/design_tb_inp_to_simulator.png)

**Step2:** Dumping design variables to vcd(value change dump) file

![variable_dumping_vcd_file](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day1/images_mux_2x1/functional_verification/variable_dumping_vcd_file.png)

**Step3:** Using gtkwave to visualize the variables dumped in vcd file

![view_vcd_gtkwave](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day1/images_mux_2x1/functional_verification/view_vcd_gtkwave.png)

**Step4:** Functional simulation waveform

![Functional Verification](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day1/images_mux_2x1/functional_verification/Functional_Verification.png)

**Step5:** Reading Sky130 standard cell library

![read_library](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day1/images_mux_2x1/Design_synthesis/read_library.png)

**Step6:** Reading RTL Design file

![read_design](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day1/images_mux_2x1/Design_synthesis/read_design.png)

**Step7:** Synthesizing Design

![synthesizing_design](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day1/images_mux_2x1/Design_synthesis/synthesizing_design.png)

**Step8:** Synthesized Design

![synthesized_design](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day1/images_mux_2x1/Design_synthesis/synthesized_design.png)

**Step9:** Linking synthesized Design to standard cell library 

![Design_linking](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day1/images_mux_2x1/Design_synthesis/DEsign_linking.png)

**Step10:** Using "show" command to visualise synthesized design

![cmd_to_see_synthesized_design](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day1/images_mux_2x1/Design_synthesis/cmd_to_see_synthesized_design.png)

**Step11:** View Synthesized 2x1 MUX

![view_synth_design](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day1/images_mux_2x1/Design_synthesis/view_synth_design.png)

**Step12:** Using write_verilog command to write gate level netlist to a file

![write_gate_level_netlist](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day1/images_mux_2x1/Design_synthesis/write_gate_level_netlist.png)

**Step13:** Gate Level Netlist for 2x1 MUX 

![gate_level_netlist](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day1/images_mux_2x1/Design_synthesis/gate_level_netlist.png)    
