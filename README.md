# 🛡️ KAVACH  
### A Containerized CAD Framework for Bit-Flip Logic Obfuscation
---
## 📌 Overview
KAVACH is a containerized, plug-and-play CAD framework for automated bit-flip logic obfuscation integration and adversarial evaluation for hardware integrity protection.
---

## 🎯 Repository Purpose

This public repository is intended **for reviewer**.

It contains runtime and memory statistics for 
- Oracle-guided SAT attack logs  
- Learning-guided structural attack outputs (SCOPE, SWEEP)  
- Combined logical–physical probing (CLAP) traces    

## 📂 Repository Structure
```bash
Attack_Log/
|
├── benchmark/
|   ├── CLAP_<benchmarkname>K<keysize>.txt
|   ├── SCOPE<benchmarkname>K<keysize>.txt
|   └── SWEEP<benchmarkname>_K<keysize>.txt
|
└── README.md
```


## ⚙ Experimental Configuration
All experiments correspond to Section 4 of the manuscript
- UC Berkeley ABC (netlist processing)
- Synopsys Design Compiler (28nm, 7-track standard-Vt)
- CentOS-based environment
- Intel Xeon CPU
- 64 GB RAM
- Key sizes: 32-bit and 64-bit
