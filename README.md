# The ECG Towel

*A concept for pre-hospital high-density cardiac mapping*

## The idea

A paramedic reaches a patient with a misbehaving heart and has twelve electrical viewpoints to work with — the standard 12-lead ECG. Hours later, a hospital electrophysiology lab could map that same heart in three dimensions with hundreds of virtual electrodes. This concept paper asks whether that gap can be closed: a flexible, high-density electrode wrap (informally, an ECG towel) applied at the roadside in a couple of minutes, establishing its own geometry without a CT scan, and sending a 3D cardiac map ahead to the receiving hospital.

## What makes it nearly possible

- **Imageless cardiac mapping is real**: Corify Care's ACORYS system performs ECGI without CT or MRI, using a statistical shape model — clinically validated and FDA-cleared. The hardest prerequisite has been demonstrated by others, in the clinic.
- **Pre-hospital ECG already saves lives**: earlier diagnosis measurably improves outcomes; the pathway is proven.
- **Flexible high-density arrays are emerging** in the materials literature — though ECGI reconstruction accuracy remains contested, and that caveat transfers here in full.

**What nobody has done**: taken high-density ECGI into the ambulance. No pre-hospital deployment, no rapid-apply form factor, no motion-tolerant pipeline was found in the searches behind this paper. That combination is the entire subject.

## The hard problems, honestly stated

1. **Motion noise** — everything published on ECGI comes from stationary patients in quiet rooms. Whether micro-volt signals survive a moving ambulance is completely unevidenced. This is the gating question.
2. **Does density pay?** — ACORYS works with 63 electrodes. Whether hundreds of imperfect contacts beat tens of good ones is an open research question, not a settled advantage.
3. **Contact, skin, and bodies** — clustered electrode failures and demographic validity.
4. **The decision-support boundary** — regulatory posture is designed fail-safe but untested.

The paper closes with three cheap experiments, each with an explicit kill condition. Two of them need no new hardware.

## About the previous version

The earlier document in this repository was styled as an investment memorandum. It has been **withdrawn**: alongside legitimate engineering analysis, it contained personnel, advisory, and market-diligence claims that had no basis in reality — artefacts introduced during AI-assisted drafting. No advisors were engaged, no letters of intent obtained, no applications submitted, no interviews conducted, and no one has been contacted regarding this work. This concept paper replaces it and carries only what can be defended.

## Documentation

See [`ECG_Towel_v7.0.pdf`](ECG_Towel_v7.0.pdf) for the full concept paper.

## Contributing

Criticism is more useful than endorsement — ECGI researchers, signal-processing engineers, paramedics, and regulatory specialists are all better placed than the author to kill or advance specific parts of this concept. Open an issue or write directly.

## License

MIT License — see [LICENSE](LICENSE).

## Contact

Aaron Garcia
aaron@garcia.ltd
