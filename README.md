<p align="center">
  <img src="https://img.shields.io/badge/Status-Pre--Prototype-orange?style=for-the-badge" alt="Status: Pre-Prototype"/>
  <img src="https://img.shields.io/badge/Funding-Seeking%20£15M-blue?style=for-the-badge" alt="Funding: Seeking £15M"/>
  <img src="https://img.shields.io/badge/Electrodes-700-brightgreen?style=for-the-badge" alt="Electrodes: 700"/>
</p>

<h1 align="center">⚡ HD-ECGI</h1>
<h3 align="center">High-Density Electrocardiographic Imaging System</h3>

<p align="center">
  <strong>Bringing electrophysiology lab precision to the back of an ambulance.</strong>
</p>

<p align="center">
  <em>No CT scanner. No hospital. Just a vest and 90 seconds.</em>
</p>

---

## 🎯 The Problem

Every year, **30,000 people in the UK** die from sudden cardiac arrest before reaching hospital. Paramedics have one tool: the 12-lead ECG — technology essentially unchanged since 1942.

Meanwhile, in hospital EP labs, cardiologists use 252-electrode systems with CT-derived heart geometry to map cardiac electrical activity in stunning 3D detail.

**The gap is fatal.**

## 💡 The Insight

What if you didn't need CT?

Our hypothesis: **700 electrodes + statistical shape modelling = CT-free geometry estimation** accurate enough for pre-hospital use.

If we're right, this unlocks portable EP-grade cardiac mapping for the first time in history.

If we're wrong, we pivot to hospital-based systems and compete on electrode density.

## 🔬 Technical Specs

| Parameter | Target | Evidence Level |
|-----------|--------|----------------|
| Electrode Count | **700** | Design spec |
| Sampling Rate | 4000 Hz/channel | Validated |
| CT-free Accuracy | ±20mm | **Hypothesis** |
| Deployment Time | <120 seconds | Requires validation |
| Weight | <5 kg | Mass budget complete |
| Battery | 4 hours continuous | 15W power budget |

## 📊 What Success Looks Like

```
┌─────────────────────────────────────────────────────────────┐
│  SCENARIO              NPV        PROBABILITY    EXPECTED   │
├─────────────────────────────────────────────────────────────┤
│  Full Success         £42M           15%         +£6.3M     │
│  Hospital Only        £18M           25%         +£4.5M     │
│  CT-Based Pivot        £5M           30%         +£1.5M     │
│  Component Sale       -£8M           10%         -£0.8M     │
│  Total Failure       -£15M           20%         -£3.0M     │
├─────────────────────────────────────────────────────────────┤
│  EXPECTED NPV                       100%         +£1.3M     │
└─────────────────────────────────────────────────────────────┘
```

**Break-even: 8% success probability. We estimate 15%.**

## 🚦 Development Gates

| Month | Gate | Criterion | If Fail |
|-------|------|-----------|---------|
| **3** | Benchtop PoC | 64-ch optical mux <50μs skew | **TERMINATE** |
| 6 | Optical Engineer | Primary or backup secured | PAUSE |
| 9 | CT Data Access | ≥300 scans for training | PAUSE |
| 12 | Market Validation | N≥50 WTP study positive | PIVOT REVIEW |
| **18** | CT-Free Algorithm | ±30mm accuracy (N≥100) | **PIVOT** |

We kill fast. We pivot faster.

## 🛡️ What We're Not

- ❌ **Not a diagnosis machine** — Clinical Decision Support only
- ❌ **Not autonomous** — Human-in-loop required
- ❌ **Not validated** — All performance figures are engineering targets
- ❌ **Not built** — This is a pre-prototype investment proposal

## 📁 Repository Contents

```
HD-ECGI/
├── docs/
│   └── HD-ECGI-Whitepaper-v6.docx    # Full technical proposal
├── models/
│   └── [placeholder]                  # SSM training (Phase 1)
├── firmware/
│   └── [placeholder]                  # Optical mux control (Phase 1)
├── algorithms/
│   └── [placeholder]                  # CT-free estimation (Phase 1)
└── README.md
```

## 🤝 Get Involved

**Investors:** Read the whitepaper. Grill the assumptions. Fund the hypothesis test.

**Optical Engineers:** We need you. £90-120K + equity. [Contact us](#contact).

**EP Cardiologists:** Clinical advisory board forming. Shape the product.

**NHS Trusts:** Interested in clinical validation partnership? Let's talk PACS access.

## 📄 Documentation

| Document | Description |
|----------|-------------|
| [Technical Whitepaper](docs/HD-ECGI-Whitepaper-v6.docx) | Full investment memorandum with evidence classification |
| [Liability Matrix](docs/HD-ECGI-Whitepaper-v6.docx#liability) | Who's responsible when things go wrong |
| [Demographic Validation](docs/HD-ECGI-Whitepaper-v6.docx#demographics) | How we're addressing training data bias |

## ⚠️ Honest Risks

1. **CT-free may not work.** Schulze 2019 achieved ±18mm with 12 leads. Extrapolating to 700 is conjecture.

2. **Optical multiplexing at scale is unproven.** 66% timing margin, but three components need PoC.

3. **Market validation is weak.** N=12 interviews is anecdote, not evidence. Phase 1 fixes this.

4. **Demographic bias could kill.** Training data underrepresents South Asian (4×) and obese (4×) populations.

5. **If CT-free fails, we compete against CardioInsight's 10-year head start.**

We document these risks because pretending they don't exist is how projects fail.

---

<p align="center">
  <strong>The best time to map a heart attack was in the EP lab.</strong><br/>
  <strong>The second best time is in the ambulance.</strong>
</p>

---

## 📬 Contact

**Aaron Garcia**  
aaron@garcia.ltd

<p align="center">
  <sub>Version 6.0 | December 2025 | Classification: CONFIDENTIAL</sub>
</p>
