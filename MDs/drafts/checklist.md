# RQ1 — Full Candidate Checklist & Scoping Rationale


## Full candidate list (45 items, brief form)

Legend: **[T]** = tested — one of the 29 items (28 scored + 1 qualitative flag) selected from this full framework for hands-on evaluation (see `RQ1.md` for detailed test procedure/scoring/citation) · **[N]** = not tested — part of the full candidate framework, but out of scope for hands-on testing given the 10-week constraint · source shown in brackets.


### C1 — Avatar Representation
| ID | Item | Status | Source |
|---|---|---|---|
| C1.1 | Avatar import/swap | **[T]** | Li et al., 2026 |
| C1.2 | Custom/cloned voice | **[T]** | Bai et al., 2025 |
| C1.3 | Demographic diversity of default avatar library (gender/age/ethnicity) | **[N]** | IVH Toolkit paper — Module I explicitly designed for demographic diversity |
| C1.4 | Photo-based personalised avatar generation pipeline | **[N]** | IVH Toolkit paper — Module I describes this pipeline (noted as a limitation/future work in that earlier version — worth checking if the current SDK has matured this) |
| C1.5 | Clothing/hairstyle/accessory customisation | **[N]** | IVH Toolkit paper — real user feedback explicitly requested "more styles, hair, clothes for the avatar" |
| C1.6 | Body-shape/size diversity beyond default models | **[N]** | IVH Toolkit paper — named as a known limitation of the model set |

### C2 — Speech / Verbal Behaviour
| ID | Item | Status | Source |
|---|---|---|---|
| C2.1 | Manual/scripted speech trigger | **[T]** | Bai et al., 2025 |
| C2.2 | Multilingual STT/TTS support | **[T]** | Researcher judgement (generalisability) |
| C2.3 | Interrupt/barge-in mid-speech | **[T]** | Li et al., 2026 (own pilot study finding) |
| C2.4 | Hallucination/fabrication risk | **[T]** | Bai et al., 2025 |
| C2.5 | Prosody/emotional tone control in TTS output | **[N]** | Researcher judgement |
| C2.6 | Streaming vs. full-utterance TTS latency mode | **[N]** | Li et al., 2026 — toolkit "keeps these components modular," implying multiple integration modes exist worth checking |

### C3 — Non-verbal Behaviour
| ID | Item | Status | Source |
|---|---|---|---|
| C3.1 | Manual/scripted gesture trigger | **[T]** | Li et al., 2026 |
| C3.2 | Manual/scripted facial expression trigger | **[T]** | Li et al., 2026 |
| C3.3 | Gesture/expression library breadth, persona-consistency | **[T]** | Bai et al., 2025 |
| C3.4 | Gaze behaviour / eye contact control | **[N]** | Li et al., 2026 (gaze listed as core capability); Oliva et al., 2026 also flags cultural sensitivity of continuous eye contact as an ethical/UX consideration |
| C3.5 | Individual limb/joint-level animation control (fine-grained, not just preset actions) | **[N]** | IVH Toolkit paper — real user complaint: "missing some controls, such as the left arm up and down" |

### C4 — Listening / Input
| ID | Item | Status | Source |
|---|---|---|---|
| C4.1 | External context injection bypassing live STT | **[T]** | Bai et al., 2025 |
| C4.2 | Multimodal/visual perception of environment | **[T]** | Li et al., 2026 |
| C4.3 | Real-time recognition of a real user's physical actions/gestures (e.g. video-based pose estimation feeding into agent perception) | **[N]** | IVH Toolkit paper — Module II, action classification from tracked 2D pose |
| C4.4 | Proximity/social-distance awareness | **[N]** | Li et al., 2026 — "proximity detector, which helps the IVA maintain appropriate social distance" |

### C5 — Control and Autonomy (unchanged — core category, already well-grounded)
| ID | Item | Status | Source |
|---|---|---|---|
| C5.1 | Full manual control path exists (WoZ feasibility) | **[T]** | Bai et al., 2025; Simpson et al., 2022 |
| C5.2 | Native WoZ/operator interface shipped | **[T]** | Simpson et al., 2022; Welicit paper |
| C5.3 | Persona/role constraint injection | **[T]** | Bai et al., 2025 |
| C5.4 | Role constraint reliability (Condition B) | **[T]** | Bai et al., 2025 |
| C5.5 | Decision-boundary enforcement (Condition B) | **[T]** | Bai et al., 2025 |

### C6 — Reproducibility / Logging (unchanged)
| ID | Item | Status | Source |
|---|---|---|---|
| C6.1 | Interaction logging exposed programmatically | **[T]** | Bai et al., 2025 |
| C6.2 | Deterministic replay (Condition A) | **[T]** | Ledo et al., 2018 |
| C6.3 | Session/interaction recording | **[T]** | Bai et al., 2025 |

### C7 — Technical Performance
| ID | Item | Status | Source |
|---|---|---|---|
| C7.1 | Exposed performance/latency telemetry | **[T]** | Simpson et al., 2022 |
| C7.2 | Standalone Quest 3 performance | **[T]** | Zhang et al., 2025; Bai et al., 2025 |
| C7.3 | Local vs. cloud model swap | **[T]** | Researcher judgement |
| C7.4 | Modular service architecture (swap STT/LLM/TTS independently without full rewrite) | **[N]** | Li et al., 2026 — explicitly designed as modular components "to simplify integration of emerging AI models" |

### C8 — XR Compatibility (unchanged)
| ID | Item | Status | Source |
|---|---|---|---|
| C8.1 | Fully standalone Quest 3 operation | **[T]** | Bai et al., 2025 |
| C8.2 | Headset tracking integration | **[T]** | Li et al., 2026 |

### C9 — Developer Experience
| ID | Item | Status | Source |
|---|---|---|---|
| C9.1 | Documentation clarity | **[T]** | Ledo et al., 2018 (delegated to RQ3) |
| C9.2 | Setup effort | **[T]** | Ledo et al., 2018 (delegated to RQ3) |
| C9.3 | Example usefulness | **[T]** | Ledo et al., 2018 (delegated to RQ3) |
| C9.4 | Debugging difficulty | **[T]** | Ledo et al., 2018 (delegated to RQ3) |
| C9.5 | Extensibility | **[T]** | Ledo et al., 2018 (delegated to RQ3 / dev journal) |
| C9.6 | Complexity-to-use-case fit (does the toolkit's breadth suit a narrow, focused research task, or does it feel over-engineered for it) | **[N]** | Li et al., 2026 — own end-user quote: toolkit's "large scope of out-of-the-box features was appreciated, but also described as probably too complex for narrow and specific use cases" |
| C9.7 | External usability benchmark for comparison context | **[N]** | Not a test — a citation note. IVH Toolkit paper reports a formal SUS score of 58.75 ("ok," Bangor et al. 2008 scale) for the predecessor toolkit; worth referencing as comparison context if RQ3's own usability signal comes back notably better/worse |

### C10 — Openness / Sustainability 
| ID | Item | Status | Source |
|---|---|---|---|
| C10.1 | Open-source license and repository accessibility | **[N]** | Li et al., 2026 — explicitly positions the toolkit as "transparent, extensible, and scalable" open-source alternative to closed commercial tools |
| C10.2 | Active maintenance / community contribution activity (recent commits, open issues addressed) | **[N]** | Li et al., 2026 — own users "appreciated the open-source approach and the fact that developers are encouraged to contribute" |
| C10.3 | Cost transparency (mandatory paid cloud services vs. optional/local alternatives) | **[N]** | Li et al., 2026 — explicitly contrasts itself with proprietary alternatives that are "cost-intensive" with "feature limits... which hinder development" |

---

## Count summary

| Category | Total candidate items | Selected for hands-on testing |
|---|---|---|
| C1 | 6 | 2 |
| C2 | 6 | 4 |
| C3 | 5 | 3 |
| C4 | 4 | 2 |
| C5 | 5 | 5 |
| C6 | 3 | 3 |
| C7 | 4 | 3 |
| C8 | 2 | 2 |
| C9 | 7 | 5 |
| C10 | 3 | 0 |
| **Total** | **45** | **29** (28 scored + C2.4 qualitative flag) |

---

