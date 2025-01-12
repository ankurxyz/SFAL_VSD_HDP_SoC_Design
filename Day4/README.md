# Day4: GLS, blocking vs non-blocking and Synthesis-Simulation mismatch

## 1. Post Synthesis Simulation or Gate Level Simulation
### 1.1. Ternary Mux

**Synthesized Design**

![synth_design](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day4/assets/post_synthesis_simulation/synth_ternary_oper_mux.png)

**GLS Command**

![command](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day4/assets/post_synthesis_simulation/post_synth_sim_cmd.png)

**Gate Level Simulation**

![GLS](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day4/assets/post_synthesis_simulation/waveform.png)

## 2.Synthesis and Simulation Mismatch
### 2.1. bad_mux

**RTL Design**

![Design](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day4/assets/synth_sim_masmatch/bad_mux/RTL_Design_mux.png)

**Functional Simulation**

![FV](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day4/assets/synth_sim_masmatch/bad_mux/functional_veri.png)

**Synthesized Design**

![Synth Design](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day4/assets/synth_sim_masmatch/bad_mux/synth_mux.png)

**Post Synthesis Simulation**

![GLS](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day4/assets/synth_sim_masmatch/bad_mux/post_synth_sim.png)

In bad_mux design, a non blocking statement has been used inside the always block and sensitivity list has only the select signal. Ideally for combinational logic, all the input/output signals have to be in the sensitivity list and blocking statement should be used. For these reasons a mismatch in functional simulation waveform and post synthesis simulation waveform has been observed. 

### 2.2. blocking_caveat

**RTL Design**

![Design](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day4/assets/synth_sim_masmatch/blocking_caveat/design.png)

**Functional Simulation**

![FV](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day4/assets/synth_sim_masmatch/blocking_caveat/fv.png)

**Synthesized Design**

![Synth_Design](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day4/assets/synth_sim_masmatch/blocking_caveat/design_synth.png)

**Post Synthesis Simulation**

![GLS](https://github.com/ankurxyz/SFAL_VSD_HDP_SoC_Design/blob/master/Day4/assets/synth_sim_masmatch/blocking_caveat/gls.png)

In blocking_caveat design, the output signal is assigned a logic prior to the intermediate signal which causes the output line to take garbage/earlier time stamp value. This lead to the mismatch in functional simulation waveform and post-synthesis simulation waveform.   
