<div align="center">

<!-- Header Banner (Auto-adapts cleanly on GitHub Dark & Light Mode) -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,50:112233,100:008080&height=180&section=header&text=Omar%20Islam&fontSize=46&fontColor=FFFFFF&fontAlignY=38&desc=Digital%20IC%20Design%20%7C%20RISC-V%20Architecture%20%7C%20Formal%20Verification&descSize=16&descAlignY=62&descColor=A5F3FC" width="100%" alt="Omar Islam Header"/>

<p align="center">
  <strong>Zewail City University — Nanotechnology & Nanoelectronics</strong>
</p>

<!-- Domain & Stack Badges -->
<p align="center">
  <img src="https://img.shields.io/badge/RTL-SystemVerilog_%7C_Verilog-0F172A?style=flat-square&logo=cpu&logoColor=38BDF8" alt="RTL"/>
  <img src="https://img.shields.io/badge/ISA-RISC--V_(RV32IM)-0F172A?style=flat-square&logo=riscv&logoColor=34D399" alt="RISC-V"/>
  <img src="https://img.shields.io/badge/Verification-Formal_%7C_Mutation_%7C_Co--Sim-0F172A?style=flat-square&logo=checkmarx&logoColor=FBBF24" alt="Verification"/>
  <img src="https://img.shields.io/badge/Silicon_%26_FPGA-SKY130HD_%7C_Zynq_%7C_Cyclone_V-0F172A?style=flat-square&logo=amd&logoColor=F87171" alt="Silicon & FPGA"/>
</p>

<!-- Quick Navigation Anchor Bar -->
<p align="center">
  <a href="#-engineering-architecture">Architecture</a> •
  <a href="#-featured-silicon--verification-projects">Featured Projects</a> •
  <a href="#-verification-sign-off-matrix">Measured Results</a> •
  <a href="#-verification-methodology">Philosophy</a> •
  <a href="#-active-silicon-roadmap">Active Tapeouts</a>
</p>

</div>

> [!IMPORTANT]
> **Core Engineering Principle:** A design is not validated simply because it passes its tests. Its correctness must be supported by **independent, reproducible evidence** — *build the design, build an independent way to challenge it, measure the evidence, and document the limits.*

---

## ⚡ Engineering Architecture

I design, implement, and verify digital hardware systems—bridging processor microarchitecture, SoC integration, hardware accelerators, and rigorous verification infrastructure, alongside machine learning built from first principles.

```systemverilog
module omar_islam #(
    parameter INSTITUTION = "Zewail City University — Nanotechnology & Nanoelectronics",
    parameter TARGET_PDK  = "SKY130HD",
    parameter TARGET_FPGA = "Zynq-7010 | Intel Cyclone V"
)(
    input  logic architectural_spec_i,
    input  logic algorithmic_model_i,
    output logic verified_silicon_o
);

    // Core Domains:
    // [1] Digital RTL & SoC   : RV32IM pipelines, AXI4 crossbars, 4-core MESI coherence
    // [2] Hardware Compute    : 8x8 INT8 systolic arrays, quantized LeNet-5, Keccak crypto
    // [3] Verification Infra  : Reference co-sim, unbounded formal proofs, mutation testing
    // [4] ASIC / FPGA Flow    : RTL-to-GDSII, DFT fault coverage, PPA sign-off, FPGA boot

    // Engineering Sign-Off Invariant:
    property p_justified_confidence;
        @(posedge clk)
        passing_tests |-> (independent_oracle_match && formal_proven && mutation_qualified);
    endproperty

    assert property (p_justified_confidence)
        else $error("Verification Gap: Passing tests alone do not prove correctness.");

endmodule
```

<details>
<summary><b>🔍 Expand Full Technical Domain Matrix</b></summary>
<br>

| Domain | Areas of Work |
| :--- | :--- |
| **Digital RTL Design** | RISC-V processors, pipelined datapaths, accelerators, memory interfaces |
| **Design Verification** | Golden-model comparison, constrained testing, scoreboards, mutation testing |
| **Formal Methods** | Model checking, protocol properties, exhaustive state-space exploration |
| **SoC Architecture** | Processor–accelerator integration, AXI interconnects, cache coherence |
| **ASIC Implementation** | RTL-to-GDSII workflows, SKY130HD, PPA evaluation, DFT |
| **FPGA Prototyping** | Functional validation and implementation on physical FPGA platforms |
| **Hardware-Oriented ML** | Quantized inference, systolic computation, neural networks from scratch |

</details>

---

## 🛠️ Featured Silicon & Verification Projects

### 1. Processor Architecture & SoC Integration

<table>
<tr>
<td width="50%" valign="top">

#### 🔹 [Cascade SoC](https://github.com/3more102/cascade-soc)
<kbd>RISC-V SoC</kbd> <kbd>INT8 Accelerator</kbd> <kbd>SKY130HD</kbd> <kbd>DFT</kbd>

RISC-V System-on-Chip integrating processor architecture, custom INT8 acceleration, and system-level verification.
- **4 independent** integration-verification approaches
- **DFT implementation** with measured fault coverage
- **RTL-to-GDSII** targeting the SKY130HD standard-cell library
- *Status: Physical implementation & place-and-route in progress*

</td>
<td width="50%" valign="top">

#### 🔹 [Cascade RV32I](https://github.com/3more102/cascade-rv32i)
<kbd>RV32IM</kbd> <kbd>5-Stage Pipeline</kbd> <kbd>FPGA Booted</kbd> <kbd>Mutation Tested</kbd>

Five-stage pipelined RISC-V microarchitecture validated from RTL down to physical silicon execution.
- **Architectural commit-log** co-simulation vs. golden model
- **Gate-level regression** to verify synthesized behavior
- **Mutation testing** to quantify testbench strength
- **Booted on physical FPGA** hardware

</td>
</tr>
</table>

### 2. Hardware Acceleration & ASIC Design

<table>
<tr>
<td width="50%" valign="top">

#### 🔹 [Systolic Tile](https://github.com/3more102/systolic-tile)
<kbd>8×8 INT8</kbd> <kbd>64 MACs/cycle</kbd> <kbd>Cyclone V</kbd> <kbd>Zynq-7010</kbd>

Portable 8×8 INT8 systolic-array matrix accelerator built for deterministic arithmetic correctness.
- **64 multiply–accumulate** operations per clock cycle
- **Bit-exact validation** against a Python reference model
- **Multi-vendor FPGA builds** (Intel Cyclone V & AMD/Xilinx Zynq-7010)

</td>
<td width="50%" valign="top">

#### 🔹 [LeNet-5 ASIC Accelerator](https://github.com/3more102/lenet5-asic-accelerator)
<kbd>INT8 Inference</kbd> <kbd>SKY130HD GDSII</kbd> <kbd>PPA Measured</kbd>

Hardware implementation of a quantized LeNet-5 neural-network inference datapath.
- **Bit-exact comparison** against an independent Python oracle
- **Physical implementation** on SKY130HD standard cells
- **Measured PPA** (Power, Performance, and Area) post-layout

</td>
</tr>
</table>

### 3. Formal Verification & Protocol Correctness

<table>
<tr>
<td width="50%" valign="top">

#### 🔹 [Coherex](https://github.com/3more102/Coherex)
<kbd>4-Core MESI</kbd> <kbd>Model Checking</kbd> <kbd>Sequential Consistency</kbd>

Four-core MESI cache-coherence RTL system with exhaustive formal verification.
- **Exhaustive protocol model checking** of coherence invariants
- **Independent sequential-consistency** memory-ordering oracle
- **Mutation-qualified checkers** to prove checker sensitivity

</td>
<td width="50%" valign="top">

#### 🔹 [AXI Interconnect Verification](https://github.com/3more102/axi-interconnect-verif)
<kbd>AXI4 / AXI4-Lite</kbd> <kbd>2×2 Crossbar</kbd> <kbd>Unbounded Formal</kbd>

Multi-layered verification of AXI4 and AXI4-Lite 2×2 crossbar interconnects.
- **27 / 27** regression tests passing
- **14 / 14** injected mutation defects detected (100% kill rate)
- **Unbounded formal proofs** achieved for both interconnects

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### 🔹 [MutantHunt I²C](https://github.com/3more102/mutanthunt-i2c)
<kbd>I²C Master RTL</kbd> <kbd>Mutation Testing</kbd> <kbd>36/38 Killed</kbd>

I²C master RTL and mutation-driven verification benchmark measuring true testbench blind spots.
- **38 deliberately injected** RTL defects
- **36 defects caught** by the verification environment
- **2 surviving mutations** explicitly isolated and documented

</td>
<td width="50%" valign="top">

#### 🔹 [MNIST Neural Network from Scratch](https://github.com/3more102/mnist-nn-scratch)
<kbd>First Principles</kbd> <kbd>Pure NumPy</kbd> <kbd>No Autograd</kbd>

Deep learning engine built mathematically from scratch without automatic differentiation frameworks.
- **99.39%** MNIST accuracy (**99.55%** with test-time augmentation)
- **Manual backpropagation**, 2D convolution, and batch normalization
- Connects algorithm math directly to hardware-efficient compute

</td>
</tr>
</table>

---

## 📊 Verification Sign-Off Matrix

> Every figure below reflects documented implementation, configuration, and verification scope within its respective repository.

| Project | Target / Architecture | Verification & Implementation Evidence |
| :--- | :--- | :--- |
| **[Cascade SoC](https://github.com/3more102/cascade-soc)** | RV32 + INT8 Accel (`SKY130HD`) | **4 independent** integration-verification approaches; DFT fault coverage; PnR active |
| **[Cascade RV32I](https://github.com/3more102/cascade-rv32i)** | 5-Stage RV32IM Core (`FPGA`) | Architectural commit-log co-sim, gate-level regression, mutation tested, **FPGA boot** |
| **[Systolic Tile](https://github.com/3more102/systolic-tile)** | 8×8 INT8 Array (`Zynq` / `Cyclone V`) | **64 INT8 MACs/cycle**; bit-exact Python reference model comparison |
| **[LeNet-5 Accelerator](https://github.com/3more102/lenet5-asic-accelerator)** | INT8 CNN Datapath (`SKY130HD`) | Bit-exact Python oracle validation; **measured SKY130HD PPA** |
| **[Coherex](https://github.com/3more102/Coherex)** | 4-Core MESI Cache Coherence | **Exhaustive protocol model checking**, SC oracle, mutation-qualified checkers |
| **[AXI Interconnect](https://github.com/3more102/axi-interconnect-verif)** | AXI4 / AXI4-Lite 2×2 Crossbar | **27/27** tests passing; **14/14** mutants killed; **unbounded formal proofs** |
| **[MutantHunt I²C](https://github.com/3more102/mutanthunt-i2c)** | I²C Master Controller | **36/38** injected RTL defects detected; **2 survivors documented** |
| **[MNIST from Scratch](https://github.com/3more102/mnist-nn-scratch)** | CNN in Pure NumPy | **99.39%** classification accuracy (**99.55%** with TTA), zero autograd |

---

## 🔬 Verification Methodology

I treat verification as an engineering discipline with measurable outcomes rather than a final checklist. The objective is not to maximize passing test counts, but to **maximize justified confidence in the design**:

```text
  ┌──────────────────┐      ┌──────────────────────────┐      ┌─────────────────────────┐
  │   RTL Design     │─────▶│ 01. Independent Oracles  │─────▶│  02. Formal Reasoning   │
  │ (SystemVerilog)  │      │ Commit-log / Python ref  │      │ Exhaustive model check  │
  └──────────────────┘      └──────────────────────────┘      └─────────────────────────┘
                                                                           │
  ┌──────────────────┐      ┌──────────────────────────┐                   ▼
  │ 05. Measured     │◀─────│ 04. Cross-Level Sign-Off │◀─────┌─────────────────────────┐
  │    Evidence      │      │ RTL → Synth → Gate → HW  │      │ 03. Mutation Testing    │
  └──────────────────┘      └──────────────────────────┘      │ Verify the testbench!   │
                                                              └─────────────────────────┘
```

- **01 — Independent Reference Models:** Compare DUT behavior against separate software or architectural models to eliminate implementation-derived blind spots.
- **02 — Formal Reasoning:** Use formal properties and exhaustive model checking to prove invariants across state spaces directed simulation cannot reach.
- **03 — Verification of the Verification Environment:** Inject deliberate RTL defects to measure testbench sensitivity; treat surviving mutations as actionable evidence of verification limits.
- **04 — Cross-Level Validation:** Validate equivalence across RTL simulation, synthesis, gate-level regression, and physical FPGA/ASIC execution.
- **05 — Measurable Engineering Evidence:** Report exact proof statuses, mutation kill ratios, PPA metrics, and known architectural boundaries.

---

## 🚀 Active Silicon Roadmap

> *Ongoing engineering milestones — tracked transparently prior to completed silicon claims.*

| Milestone | Target Platform | Pipeline Stage | Current Focus |
| :--- | :--- | :--- | :--- |
| **Cascade SoC** | `SKY130HD` (130nm ASIC) | `[████████░░] 80%` — **Physical PnR** | Completing RTL-to-GDSII physical implementation, timing closure, and sign-off |
| **Keccak Tile** | `Tiny Tapeout` (ASIC) | `[█████░░░░░] 50%` — **RTL & Verification** | Transitioning validated cryptographic golden model to synthesizable RTL & formal/sim verification |

---

<div align="center">
  <sub><b>Engineering Interests:</b> RISC-V Microarchitecture • SoC Design • Digital ASIC & RTL Verification • Formal Methods • Cache Coherence & Interconnects • ML & Crypto Hardware Accelerators • DFT & Silicon Validation</sub>
</div>
