# RQ4 — Developer Experience Evaluation

## 1. Research question

**RQ4: What is the developer experience of using the IVA SDK for this doppelgänger research use case?**

### Operational form

Can developers with different levels of IVA SDK familiarity use the SDK to build a minimal doppelgänger prototype, and where do they encounter difficulties?

---

## 2. Purpose and scope

RQ4 evaluates the **usage** of the IVA SDK rather than rechecking whether individual capabilities exist. Following Ledo et al.'s usage-evaluation strategy for HCI toolkits, the study examines who can use the toolkit, which development tasks they can complete, the workflow they follow, and the difficulties they encounter.

The study focuses on:18

- whether each participant can complete a small doppelgänger authoring task;
- the time and assistance required for each task stage;
- errors, confusion, blockers and workarounds;
- the usefulness of the SDK documentation, samples and Inspector controls;
- how the observed workflow differs across the three familiarity cases;
- whether the final development experience supports or limits the SDK's suitability as a doppelgänger research platform.

This is a **small descriptive usage study with three contrasting developer cases**. It is not a controlled experiment and will not make statistical or causal claims about experience groups.

---

## 3. Relationship to the Main RQ and RQ1

The Main RQ asks whether the IVA SDK is suitable as a research platform for controlled doppelgänger experiments in XR.

- **RQ1** establishes which doppelgänger-relevant capabilities the SDK technically provides and where its boundaries lie.
- **RQ4** establishes whether developers can realistically use a selected subset of those capabilities to create a minimal doppelgänger prototype.

The participant task is derived directly from the preliminary RQ1 findings:

| RQ4 task component | RQ1 finding used to justify it |
|---|---|
| Configure an available avatar | C1.1 — Partially supported |
| Create an agent that can speak/respond | C2.1 — Supported |
| Configure identity, role and communication style | C5.2 — Supported |
| Trigger one specific gesture through code | C3.1 — Supported |
| Use the SDK documentation, samples and configuration workflow | Observed directly in RQ4 |

The task deliberately does **not** require:

- a native Wizard-of-Oz operator interface, because C5.1 found none;
- cloned voice creation or third-party account registration;
- reliable enforcement of hard persona constraints, because persona-constraint reliability testing was scoped out as future work following the Week 6 supervisor meeting;
- headset face or hand tracking, because C8.2 found no native SDK-level integration;
- a standalone Quest build, because Quest deployment is verified separately under RQ1 and would add hardware/build friction unrelated to the authoring task.

---

## 4. Evaluation target and version control

The formal RQ4 study uses:

- **IVA SDK version:** v3.0.0;
- **Core SDK commit:** `631396d`;
- **Environment:** the same prepared Unity project and computer for all participants where possible;
- **Version policy:** the project and SDK version are frozen once the first session begins.

Earlier exploratory work using v2 is background only and is not mixed with the formal RQ4 data.

---

## 5. Participants

Three developer cases are purposively selected to represent different levels of familiarity with the IVA SDK:

| Case | Experience profile | Perspective provided |
|---|---|---|
| P1 — Experienced case | The researcher, with extensive IVA SDK experience | Experienced development workflow |
| P2 — Intermediate case | A developer who has previously used the IVA SDK | Returning-user experience |
| P3 — New-user case | A developer with Unity/C# experience but no previous IVA SDK experience | First-use experience |

The different familiarity levels provide contrasting perspectives on the SDK’s developer experience. They are not treated as experimental groups, and no statistical comparison is made between them.

The two external participants provide informed consent before taking part.


### Sampling and interpretation

Participants are recruited purposively from accessible developers or project-group peers. With one case at each familiarity level, the study will not claim that the cases represent all developers. The experience labels contextualise the observations; they are not independent variables for statistical comparison.

P1's researcher case will be reported separately and interpreted cautiously because prior knowledge and involvement in the dissertation introduce bias.

---

## 6. Study scenario

> You cannot attend a short project meeting. Use the IVA SDK to create a minimal virtual stand-in that can represent you in the meeting. The stand-in should have a chosen appearance, identify its role, use a simple communication style, respond to speech, and perform one controlled greeting behaviour.

The task represents a **minimal doppelgänger prototype**, not a high-fidelity digital clone. Participants may use a fictional name, role and communication style. No private, sensitive or biometric information is required.

---

## 7. Study environment

Each participant receives the same:

- computer and Unity version, where possible;
- Unity project with IVA SDK v3.0.0 already imported;
- dependencies already downloaded and resolved;
- basic scene/XR project configuration;
- working temporary API configuration supplied by the researcher;
- access to all official SDK resources, including the README, documentation, sample scenes, Inspector descriptions and code comments;
- written task sheet and the same time limit.

The participant task begins **after package installation and API account setup**. These steps are excluded because downloads, account registration and external-service delays would dominate a short session. The researcher's own development journal records installation, dependency and initial configuration issues separately.

Participants complete and validate the authoring task in the Unity Editor. Building a standalone Quest APK is outside RQ4 and is recorded separately in RQ1.

---

## 8. Participant task

Participants have **30 minutes** for the development task. They may consult all supplied official SDK resources. They should think aloud while working, describing what they expect, what they are searching for and anything they find confusing.

### Goal 1 — Create a working agent

Add and configure an IVA in the provided scene so that:

- the agent is visible;
- the application enters Play Mode without a blocking error;
- the agent can receive one spoken input and produce one spoken response.

**Completion criterion:** one successful voice interaction is observed.

### Goal 2 — Configure a minimal doppelgänger identity

Using available SDK assets and configuration options:

- select an available compatible avatar to represent the participant;
- configure a preferred or fictional name;
- configure a meeting role;
- define a simple communication style, such as concise, friendly or formal;
- state that the agent is attending as the participant's stand-in.

**Completion criterion:** the configured identity, role and style are visible in the relevant SDK configuration and are used by the running agent.

### Goal 3 — Add one controlled non-verbal behaviour

Create a short script or UI control that directly calls the SDK's public gesture API so the agent performs one specific greeting action on command.

Expected SDK primitive:

```csharp
agent.PerformAction(actionName);
```

The researcher does not provide the completed script unless the participant reaches the fallback condition.

**Completion criterion:** the selected greeting action is triggered manually at least once without relying on the LLM to choose it.

### Goal 4 — Verify the stand-in

Run the prototype and perform the following checks:

1. Ask: **"Who are you, and why are you attending this meeting?"**
2. Ask one simple project-related question chosen by the participant.
3. Trigger the greeting gesture.

**Completion criterion:** the participant can demonstrate the identity/role response, one additional spoken response and the controlled gesture. This is an existence check only; repeated persona-constraint reliability testing is out of scope for this dissertation (identified as future work following the Week 6 supervisor meeting).

---

## 9. Assistance and fallback protocol

The researcher may clarify the wording of the task but should not initially explain where a specific SDK function or setting is located.

All assistance must be recorded using the following levels:

| Level | Assistance |
|---:|---|
| 0 | No researcher assistance |
| 1 | Task wording clarified; no SDK-specific hint |
| 2 | General directional hint, such as which documentation section or component to inspect |
| 3 | Specific procedural instruction or code/API location provided |
| 4 | Prepared fallback scene or completed component supplied |

### Fallback checkpoint

If Goal 1 is not completed after **12 minutes**, the participant receives a prepared working base scene containing a functioning agent. The participant then continues with Goals 2–4. This prevents one early setup blocker from eliminating all later observations.

Receiving the fallback is recorded as Level 4 assistance, and Goal 1 is marked incomplete/assisted rather than independently completed.

If a technical failure outside the participant's control prevents continuation, the researcher records the failure, restarts from a clean project once, and notes the incident separately.

---
## 10. Procedure

| Phase | Activity | Approximate time |
|---|---|---:|
| 1 | Introduction, consent and background questions | 3–4 minutes |
| 2 | Development task with think-aloud | Up to 25 minutes |
| 3 | Final artefact demonstration | 2 minutes |
| 4 | Post-task ratings and short interview | 5–7 minutes |
| **Total** |  | **Approximately 35 minutes** |

### Background questions

1. How much experience do you have with Unity/C#?
2. Have you used the IVA SDK before? If yes, what did you use it for?
3. Have you previously developed an XR or virtual-agent application?

## 11. Data collection

### 11.1 Observation record

The researcher records:

| Field | Data recorded |
|---|---|
| Goal outcome | Complete, partial or not completed |
| Time | Approximate start and completion time for each goal |
| Blockers | Errors, uncertainty, missing information and abandoned attempts |
| Resources used | README, documentation, sample scene, Inspector, code search or prior knowledge |
| Assistance | Highest assistance level and the exact help provided |
| Workarounds | Steps taken outside the expected/documented workflow |
| Think-aloud evidence | Short notes or consented quotations showing expectations and confusion |
| Final artefact | Unity scene, configuration and participant-created script |
| Technical incidents | Crashes, network problems or environment failures not caused by the participant |

Timing is recorded in approximate minutes. Second-by-second interaction logging is unnecessary.

### 11.2 Goal outcome coding

| Code | Meaning |
|---|---|
| Complete | Meets the stated completion criterion without the researcher completing it |
| Partial | Some required elements work, but the full criterion is not met |
| Not completed | No working outcome before the time limit |
| Complete with fallback | Completed only after Level 4 assistance; reported separately from independent completion |

### 11.3 Post-task ratings

Participants answer each statement on a five-point scale.

`1 = strongly disagree` and `5 = strongly agree`:

1. I found it easy to create the minimal virtual stand-in.
2. The SDK documentation and samples helped me complete the task.
3. The SDK's configuration options were easy to discover.
4. The code-level behaviour API was understandable.
5. I would feel confident repeating this task without assistance.
6. The SDK provides a practical starting point for doppelgänger research prototypes.

Because `n = 3`, individual ratings will be reported descriptively. They will not be used for inferential statistics or treated as a validated usability scale.

### 11.4 Post-task interview

1. What was the easiest part of the task?
2. What was the most difficult or confusing part?
3. Which resource helped you most, and why?
4. Was there anything you expected the SDK to provide but could not find?
5. Did you need any workaround that you did not initially expect?
6. Did the process feel like creating a doppelgänger, or only a generic virtual agent? Why?
7. What would you change to make this task easier for researchers?
8. Is there anything else about the development experience that the task did not capture?

The researcher may ask short follow-up questions to clarify a concrete incident observed during the task.

---

## 12. Researcher development journal

The researcher's journal complements the three task cases by recording work that is intentionally excluded from the participant session:

- installing and upgrading the SDK;
- moving from v2 to the frozen v3.0.0 release;
- dependency and API credential setup;
- inspecting documentation and samples;
- preparing the common starter project;
- creating and testing the fallback scene;
- Quest build/deployment attempts;
- undocumented steps, errors and workarounds;
- time spent on major preparation stages.

The journal is used as contextual evidence, not combined with external-participant ratings as if it were independent participant data.

---

 
## 13. Analysis Plan
 
The results will be analysed using a descriptive cross-case comparison.
 
After all three sessions, the researcher will compare the cases in one table:
 
| Finding | P1 Experienced | P2 Intermediate | P3 New user |
|---|---|---|---|
| Goals completed |  |  |  |
| Total task time |  |  |  |
| Highest assistance level |  |  |  |
| Main blocker |  |  |  |
| Resources used |  |  |  |
| Workaround required |  |  |  |
| Confidence repeating the task |  |  |  |
| Final outcome |  |  |  |
 
The analysis will identify:
 
- which parts of the task were straightforward;
- where participants encountered difficulty;
- which documentation or samples were useful;
- which steps required assistance or workarounds;
- whether prior SDK familiarity appeared to affect the observed workflow.
Because there is only one case at each familiarity level, the findings will be reported descriptively rather than statistically.
 
---

## 14. Expected reporting format

### Results table

| Participant | Experience | Goals completed | Total task time | Highest assistance | Main blocker | Final outcome |
|---|---|---:|---:|---:|---|---|
| P1 | Experienced |  |  |  |  |  |
| P2 | Intermediate |  |  |  |  |  |
| P3 | New user |  |  |  |  |  |

The written Results section will then organise findings into three to five themes supported by case evidence and short anonymised quotations where consent permits.

---

## 15. Validity and limitations

- The sample is small and purposive, so findings are descriptive rather than generalisable.
- There is only one case at each familiarity level; experience-level differences cannot be isolated from individual differences.
- P1 is the researcher and therefore cannot provide an independent view of the SDK.
- Pre-installing dependencies removes part of the first-use experience; this is mitigated by reporting installation and setup separately in the researcher journal.
- A 30-minute task covers only a small subset of the SDK and cannot represent long-term use.
- The prepared environment improves consistency but may be easier than adopting the SDK in a completely new project.
- Think-aloud may slow participants or change their normal workflow.
- Cloud-model behaviour and network conditions may affect whether the final interaction succeeds; technical incidents are therefore recorded separately from authoring difficulties.

These limitations will be stated explicitly when answering the Main RQ.

---

## 16. Ethics and data handling

Before recruitment or data collection, confirm that the dissertation's approved ethics procedure covers developer observation, think-aloud comments, artefact collection and any audio/screen recording.

- participation is voluntary;
- participants may stop without giving a reason;
- use IDs P1–P3 rather than names in the dissertation;
- do not request real personal, biometric or confidential meeting information;
- allow fictional identity details in the prototype;
- collect audio or screen recordings only with explicit consent;
- store consent information separately from research notes;
- follow the university-approved storage, retention and withdrawal process;
- remove temporary API credentials from participant copies after the session.

If recording is not covered or a participant does not consent, collect written observation notes and the final Unity artefact only.

---

## 17. Materials to prepare before the first session

- [ ] Freeze and record the IVA SDK v3.0.0 project version.
- [ ] Create one clean master project and one copy per participant.
- [ ] Confirm that the master project opens without package errors.
- [ ] Confirm that the temporary API configuration works.
- [ ] Prepare a basic scene/XR configuration without a completed IVA task.
- [ ] Prepare and test the Goal 1 fallback scene.
- [ ] Prepare the participant task sheet without API answers or completed code.
- [ ] Prepare the observation sheet and timer.
- [ ] Prepare the post-task ratings and interview questions.
- [ ] Confirm consent and ethics materials.
- [ ] Pilot the complete protocol once and adjust only obvious wording or environment problems before formal Session 1.
- [ ] Use the same final protocol for P1–P3 and record any unavoidable deviation.

---

## 20. Methodological basis

- Ledo et al. (2018), *Evaluation Strategies for HCI Toolkit Research*: usage evaluations examine who can use a toolkit, which tasks remain difficult, and combine task performance with observation, Likert feedback and open-ended interviews.
- Bai et al. (2025), *I Can't Join, but I Will Send My Agent: Stand-in Enhanced Asynchronous Meetings*: provides the motivating virtual stand-in/doppelgänger meeting scenario.
- Li et al. (2026), *A Toolkit for Creating Intelligent Virtual Humans in Extended Reality*: describes the evaluated IVA SDK and its multimodal authoring capabilities.

---

# Appendix A — Facilitator script

## Opening

> Thank you for taking part. This study evaluates the IVA SDK, not your programming ability. You will have 30 minutes to create a minimal virtual stand-in in a prepared Unity project. Please say what you are thinking while you work, especially what you expect to happen, where you look for information and what you find confusing. You may use the official SDK documentation and samples provided. I will not initially tell you where a particular setting or API is located, but I may provide recorded assistance if you become blocked. You may stop at any time.

## Before starting the timer

- confirm consent;
- confirm whether notes, audio and/or screen recording are permitted;
- assign the participant ID;
- ask the four background questions;
- open a clean participant copy of the project;
- confirm that external services and the microphone are available;
- give the participant the task sheet in Appendix B;
- answer questions about task wording only;
- start the timer.

## During the task

- do not teach the SDK unless assistance is required;
- note the resource consulted and the reason for consulting it;
- record errors using the participant's words where possible;
- at 12 minutes, apply the Goal 1 fallback if required;
- record every hint immediately with its assistance level;
- announce five minutes remaining;
- stop the development task at 30 minutes and preserve the current artefact.

## Closing

> The task is now complete. Please show me what currently works. After that, I will ask a few short questions about the process. There are no right or wrong answers; I am interested in what the SDK made easy or difficult.

---

# Appendix B — Participant task sheet

## Scenario

You cannot attend a short project meeting. Create a minimal virtual stand-in that can represent you. You may use fictional identity details; do not enter private or sensitive information.

You have 30 minutes. You may use the supplied official SDK documentation, README, samples, Inspector descriptions and code comments. Please think aloud while working.

## Tasks

### 1. Working agent

- Add and configure an IVA in the provided scene.
- Make the agent visible in Play Mode.
- Complete one spoken interaction with it.

### 2. Stand-in identity

- Select one available compatible avatar.
- Give the agent a preferred or fictional name.
- Give it a meeting role.
- Give it a simple communication style.
- Tell it that it is attending as your stand-in.

### 3. Controlled greeting

- Add a short script or UI control that manually triggers one specific greeting gesture through the SDK's public behaviour API.
- The gesture must be triggered by you, not selected freely by the AI.

### 4. Final check

- Ask: "Who are you, and why are you attending this meeting?"
- Ask one simple project-related question of your choice.
- Trigger the greeting gesture.

Tell the researcher when you believe the prototype is ready to demonstrate.

---

# Appendix C — Observation sheet

## Session information

| Field | Entry |
|---|---|
| Participant ID |  |
| Date/time |  |
| Session language |  |
| Unity experience |  |
| IVA SDK experience |  |
| XR/virtual-agent experience |  |
| Recording consent | Notes only / Audio / Screen |
| Project/SDK version |  |

## Goal record

| Goal | Start | End | Outcome | Assistance level | Resources used | Main issue/evidence |
|---|---:|---:|---|---:|---|---|
| G1 Working agent |  |  |  |  |  |  |
| G2 Stand-in identity |  |  |  |  |  |  |
| G3 Controlled greeting |  |  |  |  |  |  |
| G4 Final verification |  |  |  |  |  |  |

## Assistance log

| Time | Level | Exact assistance provided | Why it was needed |
|---:|---:|---|---|
|  |  |  |  |

## Incident and resource log

| Time | Participant action or comment | Resource/component | Interpretation for later coding |
|---:|---|---|---|
|  |  |  |  |

## Final artefact check

| Element | Yes | Partial | No | Notes |
|---|:---:|:---:|:---:|---|
| Agent visible and running |  |  |  |  |
| Spoken input and response |  |  |  |  |
| Avatar selected/configured |  |  |  |  |
| Name and role configured |  |  |  |  |
| Communication style configured |  |  |  |  |
| Stand-in identity demonstrated |  |  |  |  |
| Manual greeting gesture demonstrated |  |  |  |  |

## Observer summary

- Main success:
- Main blocker:
- Most useful resource:
- Unexpected workaround:
- Highest assistance level:
- Important quotation:
- Technical incident outside participant control:

---

# Appendix D — Post-task response form

## Ratings

`1 = strongly disagree`, `5 = strongly agree`

| Statement | 1 | 2 | 3 | 4 | 5 |
|---|:---:|:---:|:---:|:---:|:---:|
| I found it easy to create the minimal virtual stand-in. |  |  |  |  |  |
| The SDK documentation and samples helped me complete the task. |  |  |  |  |  |
| The SDK's configuration options were easy to discover. |  |  |  |  |  |
| The code-level behaviour API was understandable. |  |  |  |  |  |
| I would feel confident repeating this task without assistance. |  |  |  |  |  |
| The SDK provides a practical starting point for doppelgänger research prototypes. |  |  |  |  |  |

## Interview notes

1. Easiest part:
2. Most difficult/confusing part:
3. Most useful resource and why:
4. Expected but missing feature:
5. Unexpected workaround:
6. Doppelgänger or generic agent, and why:
7. Suggested improvement:
8. Anything not captured:
