# Anthropic Fellowship Application: STEM Track

**Candidate:** Ramkumar Bharathan  
**GitHub:** [https://github.com/ramtoo-cell](https://github.com/ramtoo-cell)  
**Track:** STEM Fellows (Science and Engineering)  
**Cohort:** January 2027 (4 Months)  

---

## Statement of Purpose & Research Vision

### 1. The Core Scientific Bottleneck in Frontier AI
Frontier reasoning models (Claude 3.5 Sonnet, Claude 3 Opus) exhibit remarkable fluency across coding and basic problem solving, yet they consistently encounter severe capability breakdowns when tasked with long-horizon scientific deductions that require **strict physical, mathematical, and hardware-software invariant preservation**. 

In STEM fields—specifically distributed hardware architectures, optical systems, and post-quantum lattice cryptography—a model cannot simply "hallucinate plausibility." A single unflagged sign flip in a polynomial reduction or a 0.5 dB oversight in an optical link power margin renders the entire scientific solution invalid. To build toward an **"AI Scientist"** capable of autonomous research, we must equip models with the capacity to internally audit and maintain domain-specific invariant boundaries throughout multi-step derivations.

### 2. My Research Grounding & Domain Pedigree
My scientific work bridges theoretical algebra, hardware simulation, and machine learning systems:
* **Academic Grounding:** Master of Science in Artificial Intelligence at **Purdue University** *(in progress)*; deep command of distributed computing, hardware memory bottlenecks, and algorithmic efficiency.
* **Patented Systems IP (USPTO):** Author of patent applications covering *Disaggregated Optical Key-Value Cache Systems and Near-Memory Softmax Architectures* (eliminating GPU High Bandwidth Memory constraints in large context windows).
* **Pure Python Cryptographic Implementations:** Built zero-dependency implementations of **Ring-Learning With Errors (Ring-LWE)** Key Encapsulation Mechanisms in cyclotomic polynomial rings $\mathbb{Z}_q[x]/(x^d + 1)$ without external C/C++ dependencies.

### 3. Open Problems I Will Tackle as an Anthropic STEM Fellow
During the four-month fellowship, I will work alongside Anthropic research teams to focus on three critical open problem sets:

1. **Step-Level Derivation Soundness in Cyclotomic Ring Algebra:**
   * Developing automated evaluators that detect when models erroneously substitute standard cyclic convolution ($x^d \equiv 1$) for negacyclic reduction ($x^d \equiv -1 \pmod{x^d + 1}$) or violate discrete Gaussian noise sampling bounds ($\chi_\sigma$).
   * Building benchmarks for lattice-based primitives (Kyber / ML-KEM, Dilithium / ML-DSA).

2. **Physical Invariant Verification in Photonic AI Accelerator Architectures:**
   * Evaluating Claude's capacity to design photonic and optical interconnect architectures that respect physical constraints: insertion loss margins ($\sum \alpha_i \le \alpha_{\text{margin}}$), thermo-optic microring resonator drift ($\Delta \lambda = \frac{d\lambda}{dT}\Delta T$), and wavelength-division multiplexing (WDM) crosstalk.
   * Moving from static question-answering to dynamic simulation-in-the-loop verification harnesses.

3. **Near-Memory Softmax & Disaggregated Inference Optimization:**
   * Benchmarking Claude on distributed attention splitting across memory shards (NMAP), testing whether models can correctly derive hierarchical softmax state updates without streaming raw tensor matrices.

### 4. Supporting Open-Source Repositories
* **[`frontier-reasoning-bench`](https://github.com/ramtoo-cell/frontier-reasoning-bench):** Automated verification harnesses for polynomial ring derivations and silicon photonic link budgets.
* **[`optical-kvx-engine`](https://github.com/ramtoo-cell/optical-kvx-engine):** High-throughput optical KV-cache simulation achieving a $100,000\times$ bus traffic reduction.
* **[`quantum-agentic-suite`](https://github.com/ramtoo-cell/quantum-agentic-suite):** Pure-Python Ring-LWE KEM with intent-bound MCP tool delegation.
