# VLSI Glossary

A plain-English glossary of the acronyms and terms that fly around a chip-design
team — grouped by area, each defined in a sentence or two, with pointers to the
repos that go deeper. Built for students decoding their first datasheet, spec,
or job description.

## Design & RTL
- **RTL** — Register-Transfer Level. Describing hardware as data moving between
  registers through combinational logic each clock. Written in Verilog/SystemVerilog/VHDL. See [vlsi-verilog-examples](https://github.com/chipxpertofficial/vlsi-verilog-examples).
- **HDL** — Hardware Description Language (Verilog, SystemVerilog, VHDL).
- **FSM** — Finite State Machine; control logic as states + transitions. See [fsm-design-patterns](https://github.com/chipxpertofficial/fsm-design-patterns).
- **Netlist** — a list of cells and the wires connecting them; the output of synthesis.
- **IP** — Intellectual Property; a reusable pre-designed block (a CPU, a DDR controller).
- **SoC** — System on Chip; many IP blocks integrated on one die.

## Verification
- **DUT** — Design Under Test.
- **UVM** — Universal Verification Methodology; the standard SystemVerilog testbench framework. See [uvm-testbench-cookbook](https://github.com/chipxpertofficial/uvm-testbench-cookbook).
- **Coverage** — how much of the design/behaviour the tests exercised (code + functional).
- **Assertion / SVA** — a property the design must always satisfy, checked automatically.
- **Constrained random** — generating legal random stimulus to hit cases humans miss.

## Timing & synthesis
- **STA** — Static Timing Analysis; checks every path meets setup/hold without simulation. See [sta-timing-closure-notes](https://github.com/chipxpertofficial/sta-timing-closure-notes).
- **Setup / Hold** — data must be stable before / after the clock edge.
- **Slack** — margin by which a path meets (positive) or misses (negative) timing.
- **Synthesis** — RTL → gate netlist. See [synthesis-with-yosys](https://github.com/chipxpertofficial/synthesis-with-yosys).
- **Critical path** — the slowest path; it sets the max clock frequency.
- **Clock skew / jitter** — difference in clock arrival between points / cycle-to-cycle variation.

## Physical design
- **PnR / P&R** — Place and Route; positioning cells and wiring them.
- **Floorplan** — the top-level arrangement of blocks, pins, and power grid.
- **CTS** — Clock Tree Synthesis; building a balanced clock distribution.
- **DRC / LVS** — Design Rule Check / Layout-vs-Schematic; physical sign-off checks.
- **GDSII** — the layout file format sent to the foundry. See [rtl-to-gdsii-flow](https://github.com/chipxpertofficial/rtl-to-gdsii-flow).
- **PDK** — Process Design Kit; the foundry's rules, models, and cell libraries for a node.
- **Standard cell** — a pre-characterised gate tiled by PnR. See [cmos-circuit-design-notes](https://github.com/chipxpertofficial/cmos-circuit-design-notes).

## Test (DFT)
- **DFT** — Design for Test; logic added to make a chip testable. See [dft-scan-atpg-notes](https://github.com/chipxpertofficial/dft-scan-atpg-notes).
- **Scan chain** — flops stitched into a shift register for controllability/observability.
- **ATPG** — Automatic Test Pattern Generation.
- **MBIST** — Memory Built-In Self-Test.
- **Fault coverage** — fraction of modelled defects the test patterns catch.

## Power
- **Dynamic / Leakage power** — switching power (`αCV²f`) vs always-on static current. See [low-power-design-notes](https://github.com/chipxpertofficial/low-power-design-notes).
- **UPF** — Unified Power Format; describes power intent (domains, isolation, retention).
- **DVFS** — Dynamic Voltage and Frequency Scaling.
- **Clock gating** — stopping the clock to idle registers to save dynamic power.

## Buses & interfaces
- **AXI / APB / AHB** — ARM AMBA bus protocols (high-performance / peripheral / legacy). See [axi-protocol-examples](https://github.com/chipxpertofficial/axi-protocol-examples).
- **CDC** — Clock Domain Crossing. See [cdc-handling-guide](https://github.com/chipxpertofficial/cdc-handling-guide).
- **FIFO** — First-In-First-Out buffer, often used across clock domains.
- **RISC-V** — an open instruction-set architecture, popular for teaching and custom cores.

## Want depth, not just a definition?
Follow the links above, or start from the [VLSI interview prep](https://github.com/chipxpertofficial/vlsi-interview-prep) bank. Mentored training at [ChipXpert](https://chipxpert.in/).

## License
MIT — see [LICENSE](LICENSE). Maintained by the ChipXpert team.
