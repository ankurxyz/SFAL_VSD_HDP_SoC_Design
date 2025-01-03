# Day 2:
## Hierarchical Design Synthesis

In Hierarchical design synthesis, the sub module synthesis is not visible in the synthesized design.

**Step1:** Read sky130 standard cell library

![read_library]()

**Step2:** Read RTL Design file

![read_rtl]()

**Step3:** Synthesized Design 

![synthesized_design]()

**Step4:** Linking Synthesized design to sky130 standard cell library

![linking]()

**Step5:** Using show command to visualize the synthesized design

![show]()

**Step6:** View Synthesized Design

![view_synth]()

**Step7:** Write netlist

![write_netlist]()

**Step8:** Hierarchical netlist

![hierarchical_netlist]()

## Flattened Design Synthesis

In Flattened Design Synthesis, the whole design is synthesized in one single module.
For flattened design synthesis, after linking design to standard cell library run the below command

![flat]()

The synthesized design is flattened as shown in the below image

![view_synth_design]()

and has the following gate level netlist

![flat_netlist]()

## Sub-Module Level Synthesis

It is done when the design is very large or the synthesis tool has some limitation in handling large designs. In this methodology, different kinds of module that are used in design are synthesized separately and then replicated for their various instances.

Use below command to synthesize sub_module1

![sub_module_synth]()

This below image shows the synthesized sub_module1

![view_synth_design]()   
