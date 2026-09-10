## 0. Project Initial Briefing and Context

**Original project title:** Benchmarking the Intelligent Virtual Agent SDK as a Research Platform for Doppelgängers

This project evaluates the Intelligent Virtual Agent SDK as a platform for building controlled virtual human experiments. The intended outcome is a practical assessment of whether the SDK is suitable for future XR and virtual human studies.

- **Objective:** Evaluate the capabilities and practical boundaries of the IVA SDK for doppelgänger research use cases.
- **Method:** Literature-informed criteria selection, a structured capability evaluation, and an independent developer usage study.
- **Outcome:** A critical assessment of the SDK's suitability for controlled doppelgänger research, including its supported capabilities, practical limitations, developer experience, and recommendations for future use.

## 1. Project Introduction

**Title:** Evaluating the Intelligent Virtual Agent SDK as a Research Platform for Controlled Doppelgänger Experiments in XR

Doppelgängers and stand-in agents are virtual representations designed to resemble a particular person or act on that person's behalf. Research involving these agents requires more than realistic appearance or natural conversation. Researchers must also be able to configure the agent's identity and behaviour, understand the limits of the underlying platform, and reproduce and observe experimental interactions.

The Intelligent Virtual Agent (IVA) SDK provides tools for creating embodied and multimodal virtual agents in XR. However, its suitability for controlled doppelgänger research has not yet been independently examined from both a capability-oriented and developer-oriented perspective. This dissertation addresses that gap by evaluating the SDK across two complementary dimensions: what it supports and where its boundaries lie, and what it is like to develop with in practice.

## 2. Research Questions

**Main RQ:** To what extent is the IVA SDK suitable as a research platform for controlled doppelgänger experiments in XR?

- **RQ1:** What doppelgänger-relevant capabilities does the SDK support, and where are its practical boundaries?
- **RQ2:** What is the developer experience of using the SDK for this doppelgänger research use case?

*Note: "Controlled" refers to the researcher's ability to configure, constrain, reproduce, and observe the agent's behaviour, rather than requiring every agent action to be manually scripted.*

**Scope:** The dissertation focuses empirically on capability coverage (RQ1) and developer usage (RQ2). Questions concerning the human–AI autonomy spectrum and the reliability of persona-constrained AI behaviour were scoped during the Discover/Define phases of the project as theoretically important but empirically out of reach within the available time and resources. These questions are addressed through literature-grounded discussion and inform selected items in the RQ1 capability checklist; a fully specified but unexecuted evaluation protocol for them is presented as future work.

## 3. Literature Review — Brief Summary

The literature review is organised around three connected areas:

- **Doppelgänger identity, embodiment, and ethics** — Defines the characteristics and responsibilities of virtual stand-ins and informs the doppelgänger-relevant requirements used in RQ1.
- **Evaluation of HCI toolkits and IVA SDKs** — Provides the methodological foundation for the capability evaluation and developer usage study.
- **Control, autonomy, and persona constraints** — Explains why researcher control and behavioural boundaries matter in doppelgänger research. These concepts inform the control-related items in the RQ1 checklist and motivate the future-work evaluation protocol.

See `02.LR.md`.

## 4. Methodology Overview

The dissertation uses two complementary evaluation strategies adapted from Ledo et al. (2018), within a Double Diamond framing that positions the empirical scope as an intentional narrowing (Discover/Define) rather than an incomplete study:

| RQ | Ledo et al. (2018) Strategy | Focus |
|----|------------------------------|-------|
| RQ1 | Heuristic evaluation | A literature-informed capability checklist examining the SDK's supported functionality and practical boundaries. |
| RQ2 | Usage evaluation | Three participants with different levels of relevant experience complete a practical SDK development task using a think-aloud protocol, followed by ratings and semi-structured interviews. |

The developer study is treated as a small-scale exploratory qualitative evaluation. Its purpose is to identify usability issues, common difficulties, and differences between cases — not to support statistical inference or population-level generalisation.

## 5. Papers

- [Evaluation Strategies for HCI Toolkit Research](https://dl.acm.org/doi/10.1145/3173574.3173610)
- [I Can't Join, but I Will Send My Agent: Stand-in Enhanced Asynchronous Meetings (SEAM)](https://dl.acm.org/doi/10.1145/3770659)
- [Anthropomorphic AI: a toolkit for authoring and interacting with intelligent virtual agents for extended reality](https://doi.org/10.3389/frvir.2026.1794720)
- [I Hear, See, Speak & Do: Bringing Multimodal Information Processing to Intelligent Virtual Agents for Natural Human-AI Communication](https://api.semanticscholar.org/CorpusID:278063630)
- [A Toolkit for Creating Intelligent Virtual Humans in Extended Reality](https://www.semanticscholar.org/paper/A-Toolkit-for-Creating-Intelligent-Virtual-Humans-Mostajeran-Li/78c6d74fc984e3c89067ff9692aa1414ca4b436e)
- [Where extended reality and AI may take us: Ethical issues of impersonation and AI fakes in social virtual reality](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0340829)

---

- [Welicit: A Wizard of Oz Tool for VR Elicitation Studies](https://dl.acm.org/doi/abs/10.1007/978-3-030-85607-6_6)
- [A Wizard or a Fool? Initial Assessment of a Wizard of Oz Agent Supporting Collaborative Virtual Environments](https://dl.acm.org/doi/10.1145/3527188.3563930)
- [Prompting an Embodied AI Agent: How Embodiment and Multimodal Signaling Affects Prompting Behaviour](https://dl.acm.org/doi/10.1145/3706598.3713110)

*The Wizard-of-Oz, control-spectrum, and prompting literature is retained despite the scope narrowing: it still supports the Control and Autonomy category in the RQ1 checklist, persona-configuration and constraint-related checklist items, and the Discussion's future-work protocol.*

## 6. Document Navigation

- `02.LR.md` — Literature Review
- `03.Method.md` — Methodology
- `11.RQ1.md` — RQ1: Capability Evaluation
- `12.RQ2.md` — RQ2: Developer Experience Evaluation
- `Experiment_Protocol.md` — Developer Usage Study Protocol
- `07.Discussion.md` — Discussion, Limitations and Future Work
- `Appendix_Future_Evaluation_Protocol.md` — Optional detailed autonomy-spectrum and persona-constraint evaluation design (Control and Constraint Protocol; not executed in this dissertation)
