<div align="center">

<!-- Hero Silicon Wave Banner -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:090D16,50:0F2942,100:0D9488&height=210&section=header&text=Omar%20Islam&fontSize=50&fontColor=F8FAFC&fontAlignY=35&desc=Digital%20IC%20Design%20%26%20Verification%20%7C%20RISC-V%20%7C%20ASIC%2FFPGA%20%7C%20Formal&descSize=15&descAlignY=58&descColor=7DD3FC&animation=fadeIn" width="100%" alt="Omar Islam Header Banner"/>

<!-- Animated Terminal Subtitle -->
<a href="https://github.com/3more102">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=16&duration=2800&pause=900&color=38BDF8&center=true&vCenter=true&width=780&height=32&lines=Digital+IC+Design+%26+Verification+Engineer;RISC-V+Microarchitecture+%26+SoC+Integration;Formal+Model+Checking%2C+Mutation+Testing+%26+Co-Sim;ASIC+(SKY130HD)+%26+FPGA+Hardware+Accelerators" alt="Engineering Specialties"/>
</a>

<br/>

<!-- Affiliation & Profile Header Pills -->
<p align="center">
  <img src="https://img.shields.io/badge/Zewail_City_University-Nanotechnology_%26_Nanoelectronics-0F172A?style=for-the-badge&logo=googlescholar&logoColor=38BDF8" alt="Zewail City University"/>
  <a href="https://github.com/3more102">
    <img src="https://img.shields.io/badge/GitHub-@3more102-0F172A?style=for-the-badge&logo=github&logoColor=34D399" alt="GitHub Profile"/>
  </a>
</p>

<!-- Domain & Silicon Tooling Badges -->
<p align="center">
  <img src="https://img.shields.io/badge/SystemVerilog-0F172A?style=flat-square&logo=cpu&logoColor=38BDF8" alt="SystemVerilog"/>
  <img src="https://img.shields.io/badge/Verilog-0F172A?style=flat-square&logo=cpu&logoColor=38BDF8" alt="Verilog"/>
  <img src="https://img.shields.io/badge/RISC--V_(RV32IM)-0F172A?style=flat-square&logo=riscv&logoColor=34D399" alt="RISC-V"/>
  <img src="https://img.shields.io/badge/AXI4_%2F_AXI4--Lite-0F172A?style=flat-square&logo=buffer&logoColor=38BDF8" alt="AXI4"/>
  <img src="https://img.shields.io/badge/MESI_Cache_Coherence-0F172A?style=flat-square&logo=diagramsdotnet&logoColor=34D399" alt="MESI Coherence"/>
  <img src="https://img.shields.io/badge/Formal_Model_Checking-0F172A?style=flat-square&logo=checkmarx&logoColor=FBBF24" alt="Formal Verification"/>
  <img src="https://img.shields.io/badge/Mutation_Testing-0F172A?style=flat-square&logo=bugsnag&logoColor=F87171" alt="Mutation Testing"/>
  <br/>
  <img src="https://img.shields.io/badge/Golden--Model_Co--Sim-0F172A?style=flat-square&logo=pytest&logoColor=FBBF24" alt="Golden-Model Co-Simulation"/>
  <img src="https://img.shields.io/badge/SKY130HD_ASIC_(RTL--to--GDSII)-0F172A?style=flat-square&logo=circuitverse&logoColor=34D399" alt="SKY130HD"/>
  <img src="https://img.shields.io/badge/AMD%2FXilinx_Zynq--7010-0F172A?style=flat-square&logo=amd&logoColor=F87171" alt="Zynq-7010"/>
  <img src="https://img.shields.io/badge/Intel_Cyclone_V-0F172A?style=flat-square&logo=intel&logoColor=38BDF8" alt="Intel Cyclone V"/>
  <img src="https://img.shields.io/badge/Python_%26_NumPy_(From_Scratch)-0F172A?style=flat-square&logo=python&logoColor=FBBF24" alt="Python and NumPy"/>
  <img src="https://img.shields.io/badge/C_%2F_C%2B%2B-0F172A?style=flat-square&logo=cplusplus&logoColor=38BDF8" alt="C/C++"/>
</p>

<!-- Quick Navigation Bar -->
<p align="center">
  <a href="#-engineering-architecture">Architecture</a> •
  <a href="#-featured-engineering-projects">Featured Projects</a> •
  <a href="#-selected-measured-results">Measured Results</a> •
  <a href="#-verification-philosophy">Philosophy</a> •
  <a href="#-current-development">Current Development</a> •
  <a href="#-engineering-telemetry">Telemetry</a>
</p>

</div>

---

I design, implement, and verify digital hardware systems, with a focus on processor architectures, SoC integration, hardware accelerators, and verification infrastructure. My work also extends into machine learning from first principles, connecting algorithm-level understanding with hardware-efficient computation.

> [!IMPORTANT]
> **Core Engineering Principle:** A design is not validated simply because it passes its tests. Its correctness must be supported by **independent, reproducible evidence**. Across my projects, I use reference-model co-simulation, formal verification, mutation testing, protocol checking, and post-synthesis regression to challenge hardware implementations and assess the strength of their verification environments.

```systemverilog
// Verification Sign-Off Invariant
property p_justified_confidence;
    @(posedge clk)
    passing_tests |-> (independent_oracle_match && formal_proven && mutation_qualified);
endproperty

assert property (p_justified_confidence)
    else $error("Verification Gap: Passing tests alone do not prove correctness.");
```

---

## ⚡ Engineering Architecture

<div align="center">
  <img src="https://mermaid.ink/svg/Zmxvd2NoYXJ0IExSCiAgICBzdWJncmFwaCBFTlZbIklOREVQRU5ERU5UIFZFUklGSUNBVElPTiBBTkQgU0lHTi1PRkYgSU5GUkFTVFJVQ1RVUkUiXQogICAgICAgIHN1YmdyYXBoIFNPQ1siUHJvY2Vzc29yIGFuZCBTb0MiXQogICAgICAgICAgICBkaXJlY3Rpb24gVEIKICAgICAgICAgICAgUDFbIkNhc2NhZGUgU29DPGJyLz5SVjMyICsgSU5UOCBBY2NlbDxici8-NHggVmVyaWYgfCBERlQgfCBTS1kxMzBIRCJdCiAgICAgICAgICAgIFAyWyJDYXNjYWRlIFJWMzJJPGJyLz41LVN0YWdlIFJWMzJJTTxici8-Q29tbWl0LUxvZyB8IEZQR0EgQm9vdCJdCiAgICAgICAgZW5kCiAgICAgICAgc3ViZ3JhcGggQlVTWyJDb2hlcmVuY2UgYW5kIEJ1cyJdCiAgICAgICAgICAgIGRpcmVjdGlvbiBUQgogICAgICAgICAgICBDMVsiQ29oZXJleDxici8-NC1Db3JlIE1FU0k8YnIvPk1vZGVsIENoZWNrIHwgU0MgT3JhY2xlIl0KICAgICAgICAgICAgQzJbIkFYSSBJbnRlcmNvbm5lY3Q8YnIvPkFYSTQgLyBBWEk0LUxpdGUgMngyPGJyLz4yNy8yNyB8IDE0LzE0IHwgVW5ib3VuZGVkIl0KICAgICAgICBlbmQKICAgICAgICBzdWJncmFwaCBBQ0NbIkFjY2VsZXJhdG9ycyJdCiAgICAgICAgICAgIGRpcmVjdGlvbiBUQgogICAgICAgICAgICBBMVsiU3lzdG9saWMgVGlsZTxici8-OHg4IElOVDggfCA2NCBNQUNzL2N5Yzxici8-Q3ljbG9uZSBWICsgWnlucS03MDEwIl0KICAgICAgICAgICAgQTJbIkxlTmV0LTUgQVNJQzxici8-SU5UOCBDTk4gRGF0YXBhdGg8YnIvPlB5dGhvbiBPcmFjbGUgfCBTS1kxMzBIRCJdCiAgICAgICAgZW5kCiAgICAgICAgc3ViZ3JhcGggTUxbIlByb3RvY29sIGFuZCBNTCJdCiAgICAgICAgICAgIGRpcmVjdGlvbiBUQgogICAgICAgICAgICBNMVsiTXV0YW50SHVudCBJMkM8YnIvPkkyQyBNYXN0ZXIgUlRMPGJyLz4zNi8zOCBNdXRhbnRzIEtpbGxlZCJdCiAgICAgICAgICAgIE0yWyJNTklTVCBTY3JhdGNoPGJyLz5QdXJlIE51bVB5IC0gTm8gQXV0b2dyYWQ8YnIvPjk5LjM5JSAvIDk5LjU1JSBUVEEiXQogICAgICAgIGVuZAogICAgZW5kCgogICAgc3R5bGUgRU5WIGZpbGw6IzBiMTIyMixzdHJva2U6IzM4YmRmOCxzdHJva2Utd2lkdGg6MnB4LGNvbG9yOiNmOGZhZmMKICAgIHN0eWxlIFNPQyBmaWxsOiMwZjE3MmEsc3Ryb2tlOiMzOGJkZjgsc3Ryb2tlLXdpZHRoOjEuNXB4LGNvbG9yOiMzOGJkZjgKICAgIHN0eWxlIEJVUyBmaWxsOiMwZjE3MmEsc3Ryb2tlOiMzNGQzOTksc3Ryb2tlLXdpZHRoOjEuNXB4LGNvbG9yOiMzNGQzOTkKICAgIHN0eWxlIEFDQyBmaWxsOiMwZjE3MmEsc3Ryb2tlOiNmYmJmMjQsc3Ryb2tlLXdpZHRoOjEuNXB4LGNvbG9yOiNmYmJmMjQKICAgIHN0eWxlIE1MIGZpbGw6IzBmMTcyYSxzdHJva2U6I2MwODRmYyxzdHJva2Utd2lkdGg6MS41cHgsY29sb3I6I2MwODRmYwogICAgc3R5bGUgUDEgZmlsbDojMDcwYzE3LHN0cm9rZTojMzM0MTU1LHN0cm9rZS13aWR0aDoxcHgsY29sb3I6I2Y4ZmFmYwogICAgc3R5bGUgUDIgZmlsbDojMDcwYzE3LHN0cm9rZTojMzM0MTU1LHN0cm9rZS13aWR0aDoxcHgsY29sb3I6I2Y4ZmFmYwogICAgc3R5bGUgQzEgZmlsbDojMDcwYzE3LHN0cm9rZTojMzM0MTU1LHN0cm9rZS13aWR0aDoxcHgsY29sb3I6I2Y4ZmFmYwogICAgc3R5bGUgQzIgZmlsbDojMDcwYzE3LHN0cm9rZTojMzM0MTU1LHN0cm9rZS13aWR0aDoxcHgsY29sb3I6I2Y4ZmFmYwogICAgc3R5bGUgQTEgZmlsbDojMDcwYzE3LHN0cm9rZTojMzM0MTU1LHN0cm9rZS13aWR0aDoxcHgsY29sb3I6I2Y4ZmFmYwogICAgc3R5bGUgQTIgZmlsbDojMDcwYzE3LHN0cm9rZTojMzM0MTU1LHN0cm9rZS13aWR0aDoxcHgsY29sb3I6I2Y4ZmFmYwogICAgc3R5bGUgTTEgZmlsbDojMDcwYzE3LHN0cm9rZTojMzM0MTU1LHN0cm9rZS13aWR0aDoxcHgsY29sb3I6I2Y4ZmFmYwogICAgc3R5bGUgTTIgZmlsbDojMDcwYzE3LHN0cm9rZTojMzM0MTU1LHN0cm9rZS13aWR0aDoxcHgsY29sb3I6I2Y4ZmFmYwo=?theme=dark&bgColor=0B1222" width="100%" alt="System and Verification Architecture Flowchart"/>
</div>

<br/>

<details>
<summary><b>🔍 Expand Technical Focus Matrix (7 Core Engineering Domains)</b></summary>
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

## 🛠️ Featured Engineering Projects

### Processor Architecture & SoC Integration

<table>
<tr>
<td width="50%" valign="top">

#### 🔹 [Cascade SoC](https://github.com/3more102/cascade-soc)
<img src="https://img.shields.io/badge/Status-SKY130HD_PnR_Active-0284C7?style=flat-square" alt="Cascade SoC Status"/> <img src="https://img.shields.io/badge/Verification-4_Independent_Flows-0D9488?style=flat-square" alt="4x Verification"/>

<kbd>RISC-V SoC</kbd> <kbd>INT8 Accelerator</kbd> <kbd>SKY130HD</kbd> <kbd>DFT</kbd>

RISC-V System-on-Chip with an integrated INT8 accelerator, bringing together processor architecture, accelerator functionality, and system-level verification.
- Integration verified through **four independent approaches**
- **Design-for-test (DFT)** implementation with measured fault coverage
- **RTL-to-GDSII** implementation targeting the SKY130HD standard-cell library
- *Status: Physical implementation and place-and-route in progress*

<details>
<summary><code>View System Topology</code></summary>

```text
┌───────────────┐      ┌──────────────────────┐
│  RISC-V Core  │◀────▶│ System Interconnect  │
└───────────────┘      └──────────┬───────────┘
                                  │
                       ┌──────────▼───────────┐
                       │   INT8 Accelerator   │
                       └──────────┬───────────┘
                                  ▼
 [4 Independent Verification Approaches] + [DFT & SKY130HD PnR]
```
</details>

</td>
<td width="50%" valign="top">

#### 🔹 [Cascade RV32I](https://github.com/3more102/cascade-rv32i)
<img src="https://img.shields.io/badge/Hardware-FPGA_Booted-059669?style=flat-square" alt="FPGA Booted"/> <img src="https://img.shields.io/badge/Sign--Off-Co--Sim_%2B_Gate_%2B_Mutants-0284C7?style=flat-square" alt="Verification Scope"/>

<kbd>RV32IM</kbd> <kbd>5-Stage Pipeline</kbd> <kbd>FPGA Booted</kbd> <kbd>Mutation Tested</kbd>

Five-stage RV32IM processor verified across RTL simulation, synthesized logic, and physical FPGA execution.
- **Five-stage pipelined** RISC-V microarchitecture
- **Architectural commit-log co-simulation** against an independent golden model
- **Gate-level regression** to assess synthesized behavior
- **Mutation testing** to evaluate verification effectiveness
- **Successfully booted** on physical FPGA hardware

<details>
<summary><code>View Cross-Level Validation Flow</code></summary>

```text
[RV32IM RTL] ──▶ Commit-Log Co-Sim ◀── [Independent Golden Model]
     │
     ├──▶ Mutation Testing (Testbench Strength Evaluation)
     ├──▶ Synthesis ──▶ Gate-Level Regression
     └──▶ Physical FPGA Bitstream ──▶ Hardware Boot Verified
```
</details>

</td>
</tr>
</table>

### Hardware Acceleration & ASIC Design

<table>
<tr>
<td width="50%" valign="top">

#### 🔹 [Systolic Tile](https://github.com/3more102/systolic-tile)
<img src="https://img.shields.io/badge/Throughput-64_MACs%2Fcycle-D97706?style=flat-square" alt="64 MACs per cycle"/> <img src="https://img.shields.io/badge/Oracle-Bit--Exact_Python-059669?style=flat-square" alt="Bit-Exact"/>

<kbd>8×8 INT8</kbd> <kbd>64 MACs/cycle</kbd> <kbd>Cyclone V</kbd> <kbd>Zynq-7010</kbd>

8×8 INT8 systolic-array accelerator built for deterministic arithmetic correctness and portable hardware implementation.
- **64 multiply–accumulate** operations per cycle
- **Bit-exact validation** against a Python reference model
- **FPGA builds** targeting Intel Cyclone V and AMD/Xilinx Zynq-7010

</td>
<td width="50%" valign="top">

#### 🔹 [LeNet-5 ASIC Accelerator](https://github.com/3more102/lenet5-asic-accelerator)
<img src="https://img.shields.io/badge/Silicon-SKY130HD_PPA_Measured-059669?style=flat-square" alt="SKY130HD PPA"/> <img src="https://img.shields.io/badge/Oracle-Bit--Exact_Python-0284C7?style=flat-square" alt="Bit-Exact"/>

<kbd>INT8 Inference</kbd> <kbd>SKY130HD GDSII</kbd> <kbd>PPA Measured</kbd>

Hardware implementation of a quantized LeNet-5 neural-network inference datapath connecting quantized ML computation with measurable ASIC results.
- **Bit-exact comparison** against an independent Python oracle
- **Physical implementation** and measured power, performance, and area using SKY130HD

</td>
</tr>
</table>

### Formal Verification & Protocol Correctness

<table>
<tr>
<td width="50%" valign="top">

#### 🔹 [Coherex](https://github.com/3more102/Coherex)
<img src="https://img.shields.io/badge/Formal-Exhaustive_Model_Check-7C3AED?style=flat-square" alt="Model Checked"/> <img src="https://img.shields.io/badge/Oracle-Sequential_Consistency-059669?style=flat-square" alt="SC Oracle"/>

<kbd>4-Core MESI</kbd> <kbd>Model Checking</kbd> <kbd>Sequential Consistency</kbd>

Four-core MESI cache-coherence system focused on coherence invariants, memory-ordering correctness, and independent checker validation.
- **RTL implementation** of a multicore coherence system
- **Exhaustive protocol model checking**
- **Independent sequential-consistency oracle**
- **Mutation-qualified checkers** for verification-quality assessment

<details>
<summary><code>View Coherence Verification Topology</code></summary>

```text
 [Core 0 L1]   [Core 1 L1]   [Core 2 L1]   [Core 3 L1]
      └─────────────┴──────┬──────┴─────────────┘
                    [MESI Coherence Fabric]
                           │
        ┌──────────────────┼──────────────────┐
        ▼                  ▼                  ▼
 [Model Checker]   [SC Memory Oracle]  [Mutation Checkers]
```
</details>

</td>
<td width="50%" valign="top">

#### 🔹 [AXI Interconnect Verification](https://github.com/3more102/axi-interconnect-verif)
<img src="https://img.shields.io/badge/Formal-Unbounded_Proof-059669?style=flat-square" alt="Unbounded Proof"/> <img src="https://img.shields.io/badge/Regression_%26_Mutants-27%2F27_%7C_14%2F14-7C3AED?style=flat-square" alt="27/27 and 14/14"/>

<kbd>AXI4 / AXI4-Lite</kbd> <kbd>2×2 Crossbar</kbd> <kbd>Unbounded Formal</kbd>

AXI4 / AXI4-Lite 2×2 crossbar verified through simulation, mutation testing, and formal proof.
- **27 / 27** regression tests passing
- **14 / 14** injected mutation defects detected
- **Unbounded formal proofs** achieved for both interconnects

</td>
</tr>
</table>

### Mutation-Driven Verification & First-Principles ML

<table>
<tr>
<td width="50%" valign="top">

#### 🔹 [MutantHunt I²C](https://github.com/3more102/mutanthunt-i2c)
<img src="https://img.shields.io/badge/Mutation_Score-36%2F38_Detected-7C3AED?style=flat-square" alt="36/38 Mutants"/> <img src="https://img.shields.io/badge/Limits-2_Survivors_Documented-D97706?style=flat-square" alt="2 Survivors"/>

<kbd>I²C Master RTL</kbd> <kbd>Mutation Testing</kbd> <kbd>36/38 Detected</kbd>

I²C master RTL and mutation-driven verification environment measuring what a testbench can detect rather than relying on passing-test counts alone.
- **38 deliberately injected** RTL defects
- **36 defects detected** by the verification environment
- **Two surviving mutations** explicitly demonstrated and documented

</td>
<td width="50%" valign="top">

#### 🔹 [MNIST Neural Network from Scratch](https://github.com/3more102/mnist-nn-scratch)
<img src="https://img.shields.io/badge/MNIST_Accuracy-99.39%25_%7C_99.55%25_TTA-0284C7?style=flat-square" alt="MNIST Accuracy"/> <img src="https://img.shields.io/badge/Autograd-None_(Pure_NumPy)-0D9488?style=flat-square" alt="No Autograd"/>

<kbd>First Principles</kbd> <kbd>Pure NumPy</kbd> <kbd>No Autograd</kbd>

Neural-network implementation using NumPy without automatic differentiation, built for mathematical understanding, numerical correctness, and reproducible experimentation.
- **99.39%** MNIST classification accuracy (**99.55%** with test-time augmentation)
- **Manually implemented** backpropagation, convolution, and batch normalization
- **No autograd framework**

</td>
</tr>
</table>

---

## 📊 Selected Measured Results

| Project | Sign-Off Evidence | Verified Result |
| :--- | :--- | :--- |
| **[Cascade SoC](https://github.com/3more102/cascade-soc)** | ![4x Verif](https://img.shields.io/badge/4x_Verif_%2B_DFT-0284C7?style=flat-square) | Four independent integration-verification approaches; DFT fault coverage; SKY130HD PnR active |
| **[Cascade RV32I](https://github.com/3more102/cascade-rv32i)** | ![FPGA Boot](https://img.shields.io/badge/FPGA_Booted-059669?style=flat-square) | Golden-model and gate-level verification; mutation tested; physical FPGA boot |
| **[Systolic Tile](https://github.com/3more102/systolic-tile)** | ![64 MACs](https://img.shields.io/badge/64_MACs%2Fcycle-D97706?style=flat-square) | 64 INT8 MAC operations/cycle; bit-exact reference-model comparison |
| **[LeNet-5 Accelerator](https://github.com/3more102/lenet5-asic-accelerator)** | ![SKY130HD](https://img.shields.io/badge/SKY130HD_PPA-059669?style=flat-square) | Bit-exact validation; SKY130HD PPA measurements |
| **[Coherex](https://github.com/3more102/Coherex)** | ![Model Checked](https://img.shields.io/badge/Model_Checked-7C3AED?style=flat-square) | Exhaustive protocol model checking and mutation-qualified checkers |
| **[AXI Interconnect](https://github.com/3more102/axi-interconnect-verif)** | ![Unbounded Proof](https://img.shields.io/badge/Unbounded_Proof-059669?style=flat-square) | 27/27 tests passing; 14/14 mutation defects detected; unbounded formal proofs |
| **[MutantHunt I²C](https://github.com/3more102/mutanthunt-i2c)** | ![Mutation Score](https://img.shields.io/badge/36%2F38_Killed-7C3AED?style=flat-square) | 36/38 injected defects detected; two survivors documented |
| **[MNIST from Scratch](https://github.com/3more102/mnist-nn-scratch)** | ![Accuracy](https://img.shields.io/badge/99.55%25_TTA-0284C7?style=flat-square) | 99.39% accuracy; 99.55% with test-time augmentation |

<sub>*Each result is specific to its project's documented implementation, configuration, and verification scope.*</sub>

---

## 🔬 Verification Philosophy

I treat verification as an engineering discipline with measurable outcomes, not simply a final stage of development. **The objective is not to maximize the number of passing tests. It is to maximize justified confidence in the design.**

<div align="center">
  <img src="https://mermaid.ink/svg/Zmxvd2NoYXJ0IExSCiAgICBNMVsiMDEuIEluZGVwZW5kZW50IE1vZGVsczxici8-U2VwYXJhdGUgU1cgLyBJU0EgT3JhY2xlIl0gLS0-IE0yWyIwMi4gRm9ybWFsIFJlYXNvbmluZzxici8-RXhoYXVzdGl2ZSBNb2RlbCBDaGVja2luZyJdCiAgICBNMiAtLT4gTTNbIjAzLiBNdXRhdGlvbiBUZXN0aW5nPGJyLz5DaGFsbGVuZ2UgdGhlIFRlc3RiZW5jaCJdCiAgICBNMyAtLT4gTTRbIjA0LiBDcm9zcy1MZXZlbCBTaWduLU9mZjxici8-UlRMIHRvIFN5bnRoIHRvIEdhdGUgdG8gRlBHQSJdCiAgICBNNCAtLT4gTTVbIjA1LiBNZWFzdXJlZCBFdmlkZW5jZTxici8-UHJvb2ZzLCBQUEEgYW5kIEtub3duIExpbWl0cyJdCgogICAgc3R5bGUgTTEgZmlsbDojMGYxNzJhLHN0cm9rZTojMzhiZGY4LHN0cm9rZS13aWR0aDoycHgsY29sb3I6I2Y4ZmFmYwogICAgc3R5bGUgTTIgZmlsbDojMGYxNzJhLHN0cm9rZTojMzRkMzk5LHN0cm9rZS13aWR0aDoycHgsY29sb3I6I2Y4ZmFmYwogICAgc3R5bGUgTTMgZmlsbDojMGYxNzJhLHN0cm9rZTojYzA4NGZjLHN0cm9rZS13aWR0aDoycHgsY29sb3I6I2Y4ZmFmYwogICAgc3R5bGUgTTQgZmlsbDojMGYxNzJhLHN0cm9rZTojZmJiZjI0LHN0cm9rZS13aWR0aDoycHgsY29sb3I6I2Y4ZmFmYwogICAgc3R5bGUgTTUgZmlsbDojMGYxNzJhLHN0cm9rZTojMzhiZGY4LHN0cm9rZS13aWR0aDoycHgsY29sb3I6I2Y4ZmFmYwo=?theme=dark&bgColor=0B1222" width="100%" alt="Five-Stage Verification Methodology Flowchart"/>
</div>

<br/>

- **01 — Independent Reference Models:** Compare DUT behavior against separate software or architectural models to avoid relying exclusively on implementation-derived expectations.
- **02 — Formal Reasoning:** Use formal properties and exhaustive model checking where applicable to investigate behavior beyond directed simulation scenarios.
- **03 — Verification of the Verification Environment:** Inject deliberate defects and determine whether existing checkers detect them. Surviving mutations are evidence of verification limitations that require explanation.
- **04 — Cross-Level Validation:** Where supported by the project, validate behavior across RTL simulation, synthesis, gate-level regression, and physical FPGA implementation.
- **05 — Measurable Engineering Evidence:** Report actual test results, proof status, performance measurements, implementation results, and known limitations.

---

## 🚀 Current Development

| Milestone | Target Platform | Pipeline Stage | Objective |
| :--- | :--- | :--- | :--- |
| **Cascade SoC — Silicon Implementation** | `SKY130HD` | ![PnR](https://img.shields.io/badge/Physical_PnR-In_Progress-0284C7?style=flat-square) | Advancing the integrated RISC-V SoC through physical implementation to complete the RTL-to-GDSII flow on SKY130HD |
| **Keccak Tile — Cryptographic Hardware** | `Tiny Tapeout` | ![RTL](https://img.shields.io/badge/RTL_%26_Verification-Active-0D9488?style=flat-square) | Progressing from a validated golden model toward synthesizable RTL, independent verification, and a physical implementation submission |

<sub>*These are ongoing engineering milestones, not completed silicon claims.*</sub>

---

## 📈 Engineering Telemetry & Interests

- **RISC-V** microarchitecture and SoC design
- **Digital ASIC** design and RTL verification
- **Formal verification** and verification-quality measurement
- **Memory systems**, interconnects, and cache coherence
- **Hardware acceleration** for machine learning and cryptography
- **DFT**, physical implementation, and silicon validation

<div align="center">
  <br/>
  <a href="https://github.com/3more102">
    <img src="https://streak-stats.demolab.com?user=3more102&theme=tokyonight&hide_border=true&background=0B1222&ring=38BDF8&fire=34D399&currStreakLabel=38BDF8" alt="Omar Islam Contribution Streak"/>
  </a>
  <br/><br/>
  <a href="https://github.com/3more102">
    <img src="https://github-readme-activity-graph.vercel.app/graph?username=3more102&bg_color=0B1222&color=94A3B8&line=38BDF8&point=34D399&area=true&area_color=0284C7&hide_border=true&custom_title=GitHub%20Engineering%20Activity%20Waveform" width="100%" alt="Omar Islam Activity Waveform"/>
  </a>
</div>

> [!NOTE]
> **Build the design. Build an independent way to challenge it. Measure the evidence. Document the limits.**
> The repositories above reflect an effort to develop hardware systems that are not only functional, but also independently verifiable, reproducible, and supported by concrete engineering results.

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:090D16,50:0F2942,100:0D9488&height=95&section=footer" width="100%" alt="Footer Wave Banner"/>
