
---

# HD-ECGI System: High-Density Electrocardiographic Imaging

> **CRITICAL NOTICE:** This repository describes a medical device that does not yet exist. No prototype has been built. No clinical data exists. All performance figures are engineering targets requiring validation.
> 
> 

## 📋 Project Overview

**Version:** 6.0 (Red Team Remediated) **Classification:** Pre-Prototype Investment Proposal **Target Device:** 700-electrode rapid-deployment vest for pre-hospital emergency care.

This project aims to bridge the gap between electrophysiology laboratory precision and pre-hospital care. The HD-ECGI system utilizes optical multiplexing and novel **CT-free geometry estimation** to provide high-resolution 3D cardiac electrical mapping in the field.

## 🛠 Technical Specification

### System Architecture

The system architecture relies on three core pillars:

1. 
**High-Density Acquisition:** 700 surface electrodes.


2. 
**Optical Multiplexing:** Aggregation of signals to manage high channel counts with low latency.


3. 
**Geometry Estimation:** Statistical Shape Models (SSM) to estimate heart position without CT scans.



### Performance Targets

The following engineering specifications are defined as **[TARGET]** metrics pending validation:

| Parameter | Specification | Evidence Level |
| --- | --- | --- |
| **Electrode Count** | 700 | Design Specification |
| **Sampling Rate** | 4000 Hz/channel | [DEMONSTRATED] Standard for HD arrays |
| **ADC Resolution** | 24-bit | [DEMONSTRATED] Commercial AFE (ADS1299) |
| **CT-Free Accuracy** | ±20mm | [TARGET] vs ±18mm Schulze 2019 (12-lead) |
| **Optical Skew** | <50μs | [TARGET] 8:1 multiplexing timing budget |
| **Weight** | <5 kg | [TARGET] Component mass budget |

### Algorithms & Models

* 
**CT-Free Geometry:** Uses Bayesian priors from body habitus (height, weight, BMI) and electrode impedance patterns to constrain a Statistical Shape Model derived from N≥500 training CT scans.


* **Correlated Failure Model:** Replaces binomial independence with a spatial correlation model (). If one electrode fails, adjacent electrodes have a 51% probability of failure (cluster failure).



## 🛡️ Security & Build Pipeline

This project adheres to strict **Secure Development Lifecycle (SDL)** requirements to mitigate supply chain attacks and ensure regulatory compliance.

* **SLSA Level 3 Compliance:** Full supply chain attestation.
* **Hermetic Builds:** Bazel-based build environment with no persistent state.
* **Signing Ceremony:** Dual-person control for code signing using HSM (Yubikey FIPS).
* **Audit Trail:** Immutable, append-only logs for all build artifacts.

## ⚠️ Evidence Classification Keys

All claims in this repository's documentation are tagged according to the following evidence levels:

* **[DEMONSTRATED]** — Validated by cited peer-reviewed literature or completed work.
* **[TARGET]** — Engineering specification requiring validation.
* **[PROJECTED]** — Financial or market estimate based on assumptions.
* **[HYPOTHESIS]** — Proposition to be tested; not evidence.

## 📅 Roadmap & Development Gates

The current repository reflects **Phase 1** planning. Critical Go/No-Go decision points are defined as follows:

1. **Month 3:** Benchtop PoC (64-channel optical mux) must achieve <50μs skew.
2. 
**Month 9:** Acquisition of ≥300 CT scans for training data (via NHS PACS/SCOT-HEART).


3. **Month 12:** Market validation (N≥50) confirming willingness-to-pay.
4. **Month 18:** CT-free algorithm validation (±30mm accuracy). *Failure here triggers a Strategic Pivot to a hospital-based CT-dependent system*.



## ⚖️ Regulatory & Liability

* 
**Classification:** EU MDR Class IIb / FDA Class II (De Novo).


* **Designation:** Clinical Decision Support (CDS). The device does *not* make autonomous diagnostic decisions.


* 
**Safe Harbour:** Outputs with confidence scores <85% trigger a "LOW CONFIDENCE" alert, mandating standard-of-care assessment.



## 📂 Repository Structure

```text
03.Current/
├── docs/
[cite_start]│   ├── HD-ECGI-Whitepaper-v6.pdf    # Full Technical Proposal [cite: 1]
[cite_start]│   ├── Red-Team-Analysis.md         # Addressed findings & remediations [cite: 242]
[cite_start]│   └── Liability-Matrix.csv         # Pre-hospital liability framework [cite: 91]
├── specs/
[cite_start]│   ├── optical-timing-budget.xlsx   # Component-level timing (17μs total) [cite: 71]
│   └── power-budget.md              # Battery life calculations
├── simulation/
[cite_start]│   └── monte-carlo-failure.py       # Spatial correlation failure model (N=10k) [cite: 64]
└── compliance/
    [cite_start]└── demographic-validation.md    # Protocol for underrepresented populations [cite: 104]

