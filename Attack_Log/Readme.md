# Attack_Log

This contains the **attack execution logs** generated for the evaluation of locked benchmark circuits.

## 📁 Repository Structure

Attack_Log/
│
├── benchmark/
│ ├── CLAP_<benchname>K<keysize>.txt
│ ├── SCOPE<benchname>K<keysize>.txt
│ └── SWEEP<benchname>_K<keysize>.txt
│
└── README.md

where:
- `<benchname>` → Name of the benchmark circuit  
- `<keysize>` → Key size used in the locking scheme  
- `.txt` → Complete execution log of the attack  


## Attack Framework
The attacks were executed using the official implementations provided by the respective authors, without modification to the attack logic.
**General Meaning:**

| Symbol | Meaning |
|------|---------|
| `0` | Key bit successfully recovered as logic 0 |
| `1` | Key bit successfully recovered as logic 1 |
| `X` | Key bit could not be recovered (unknown) |

# ⚔️ Implemented Attacks

## 1. CLAP Attack
**Type:** Structural probing attack  
**Goal:** Identify and recover key bits using internal node probing and SAT-based elimination.

**Log contains:**
- Attack configuration
- Keyspace elimination statistics
- Identifiable key fractions
- Partial or full key recovery status
- Runtime information


---

## 2. SCOPE Attack
**Type:** Structural observability attack  
**Goal:** Extract partial key recovery

**Log contains:**
- COPE metric
- Candidate key extraction attempt
- Runtime statistics

---

## 3. SWEEP Attack
**Type:** Machine-learning-assisted structural attack  
**Goal:** Predict and extract key bits using circuit structural features.

**Log contains:**
- Feature weights and training statistics
- Attack execution runtime
- Extracted key result

**Features used include:**
- BDD nodes  
- Graph edges  
- Counts  
- CNF variables and clauses  
---
