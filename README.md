# Omar Islam

Hardware design and verification, with an ML-from-scratch habit on the side. Zewail City.

The theme across these repos: build the thing, then build something independent that can prove the thing wrong. Golden-model co-simulation, exhaustive model checking, mutation testing, gate-level regression — a green check here means a specific claim survived a specific attack, not that the code compiled.

## Projects

| | Proof |
|---|---|
| **[cascade-soc](https://github.com/3more102/cascade-soc)** — RISC-V SoC + INT8 accelerator | Integration-verified four independent ways, DFT'd with a measured fault-coverage number, RTL-to-GDSII flow in progress on sky130hd |
| **[cascade-rv32i](https://github.com/3more102/cascade-rv32i)** — 5-stage RV32IM core | Golden-model commit-log co-simulation, gate-level regression, and mutation testing; boots on real FPGA |
| **[systolic-tile](https://github.com/3more102/systolic-tile)** — 8×8 INT8 systolic array | 64 MAC/cycle, bit-exact against a Python golden model, FPGA builds for Cyclone V and Zynq-7010 |
| **[lenet5-asic-accelerator](https://github.com/3more102/lenet5-asic-accelerator)** — LeNet-5 int8 inference datapath | Bit-exact Python oracle, real sky130hd PPA |
| **[Coherex](https://github.com/3more102/Coherex)** — 4-core MESI cache coherence | Exhaustive protocol model checking, RTL, a sequential-consistency oracle, and mutation-qualified checkers |
| **[mutanthunt-i2c](https://github.com/3more102/mutanthunt-i2c)** — I2C master + DV environment | 38 injected RTL defects, 36 killed — both survivors proved, not excused |
| **[axi-interconnect-verif](https://github.com/3more102/axi-interconnect-verif)** — AXI4 / AXI4-Lite 2×2 crossbar | 27/27 regression, 14/14 mutation defects killed, unbounded formal proofs on both interconnects |
| **[mnist-nn-scratch](https://github.com/3more102/mnist-nn-scratch)** — neural net from raw NumPy | 99.39% on MNIST (99.55% with test-time augmentation), hand-written backprop/conv/batchnorm, no autograd |

Currently: closing `cascade-soc` through place-and-route to a real GDSII, and taking `keccak-tile` from a validated golden model toward RTL and a real Tiny Tapeout submission.
