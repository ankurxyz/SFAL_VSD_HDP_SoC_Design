# Day4: GLS, blocking vs non-blocking and Synthesis-Simulation mismatch

## 1. Post Synthesis Simulation or Gate Level Simulation
### 1.1. Ternary Mux

**Synthesized Design**

![synth_design]()

**GLS Command**

![command]()

**Gate Level Simulation**

![GLS]()

## 2.Synthesis and Simulation Mismatch
### 2.1. bad_mux

**RTL Design**

![Design]()

**Functional Simulation**

![FV]()

**Synthesized Design**

![Synth Design]()

**Post Synthesis Simulation**

![GLS]()

In bad_mux design, a non blocking statement has been used inside the always block and sensitivity list has only the select signal. Ideally for combinational logic, all the input/output signals have to be in the sensitivity list and blocking statement should be used. For these reasons a mismatch in functional simulation waveform and post synthesis simulation waveform has been observed. 

### 2.2. blocking_caveat

**RTL Design**

![Design]()

**Functional Simulation**

![FV]()

**Synthesized Design**

![Synth_Design]()

**Post Synthesis Simulation**

![GLS]()

In blocking_caveat design, the output signal is assigned a logic prior to the intermediate signal which causes the output line to take garbage/earlier time stamp value. This lead to the mismatch in functional simulation waveform and post-synthesis simulation waveform.   
