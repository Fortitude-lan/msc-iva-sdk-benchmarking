# RQ4 Developer Experience Study

## Exploratory Case Design, P2–P3 Results, and Dissertation Reporting Plan

**Working research question:** What is the developer experience of using the IVA SDK for this doppelgänger research use case?

**Study status:** P1 is the researcher/self-pilot baseline; P2 is the completed external SDK-experienced participant; and P3 is the completed external SDK-new participant. P1 data still need to be integrated or rerun under the final protocol.

---

## 1. Study purpose

This study evaluates the developer experience of using the IVA SDK to configure and extend a basic virtual stand-in prototype. It examines whether developers with different levels of relevant experience can complete the same SDK-based development tasks, how long the tasks take, where difficulties occur, and how participants perceive the SDK's usability and practical value.

The study contributes practical usage evidence to the dissertation's overall suitability judgement:

- **RQ1** establishes the SDK's doppelgänger-relevant capabilities and practical boundaries through a structured checklist.
- **RQ4** examines whether developers can use those capabilities in practice and identifies the effort, support requirements, and barriers involved.

Together, these two forms of evidence support a conditional judgement of the SDK's suitability as a platform for doppelgänger research prototypes.

---

## 2. Comparative study design

The study is a **small-scale exploratory usage evaluation across three contrasting experience profiles**. The cases follow the same task sequence and use a scaffolded Unity project, common resources, task instructions, time limit, and post-task measures. The analysis is descriptive and case-based rather than statistical.

| Participant condition | Intended experience profile | Status |
|---|---|---|
| **P1 — Researcher baseline** | Dissertation researcher with the highest project-specific and SDK familiarity; self-pilot data | Completed; data to integrate |
| **P2 — SDK-experienced external participant** | Previous experience using the IVA SDK, but not the dissertation researcher | Completed |
| **P3 — SDK-new external participant** | No previous IVA SDK or virtual-human project experience; Unity/C# background still to confirm | Completed; timing data to add |

The three profiles were defined before the final analysis, rather than created after seeing the results. The protocol supports descriptive comparison of task time, completion, assistance, errors, SUS, and reported experience.

Because there is only one case in each profile, the final analysis will not use inferential statistics or claim that experience caused any observed difference. Findings will be reported as patterns within these cases and as issues that warrant further evaluation.

P1 is not an independent external participant. P1's data represent an informed researcher/developer baseline and must be labelled separately from the external participant data. This insider position may provide useful first-hand workflow evidence, but it also creates familiarity and observer bias. P2 and P3 provide the external-user evidence.

For direct comparison, P1 must use the final `RQ4_Starter`, instructions, resources, timing rules, and success criteria used by P2 and P3. If P1's earlier self-pilot used a more complete official sample or otherwise different conditions, it should be reported as formative pilot evidence rather than entered into the formal timing comparison. P1 may rerun the final protocol to provide a comparable researcher baseline.

### Standardised conditions

All formally compared sessions should use:

- the same IVA SDK version and Unity version;
- the same `RQ4_Starter` scene;
- the same preconfigured cloud, audio, UI, animation, and dependency environment;
- the same unassigned `Agent Prefab` starting state;
- the same Goal 1–4 instructions;
- the same official SDK documentation, sample scenes, and source-code access;
- the same 30-minute development-task limit;
- the same think-aloud instructions and assistance protocol;
- the same SUS and post-task interview questions.

Any unavoidable deviation, such as remote participation, network conditions, or different hardware, should be recorded for that participant and considered when interpreting the result.

---

## 3. Tasks and collected evidence

| Goal | Task focus | Main developer-experience evidence |
|---|---|---|
| **Goal 1** | Assign and instantiate an avatar, connect the Agent, and complete one voice interaction | Initial SDK configuration, documentation use, connection problems, time, errors |
| **Goal 2** | Configure the Alex stand-in persona | Persona clarity, configuration efficiency, identity authoring |
| **Goal 3** | Add a C# script that triggers a predefined action using the public SDK API | API discoverability, coding effort, sample/source dependence, debugging |
| **Goal 4** | Demonstrate identity, project information, and manual gesture control | Final artefact integration and successful task outcome |

The complete dataset for each participant should include:

- completion status for each Goal;
- time for each Goal and total task time;
- independent completion or level of assistance;
- errors and recovery process;
- documentation, sample scenes, and source files consulted;
- relevant think-aloud observations;
- SUS responses and calculated score;
- post-task interview responses;
- verification of the final artefact.

---

## 4. Participant P2 profile

**Anonymous identifier:** P2  
**Experience condition:** Previous IVA SDK experience  
**Interpretive role:** Represents the SDK-experienced condition in the three-level comparison.

P2's result should not be presented as a first-use result. It indicates what an experienced or returning external SDK user can achieve and which barriers remain even after previous exposure to the toolkit.

---

## 5. P2 task-performance results

The corrected segmented times are reported in minutes and seconds.

| Goal | Completion | Time | Proportion of total task time |
|---|---|---:|---:|
| Goal 1 — Agent setup and voice interaction | Completed | 04:45 | 22.4% |
| Goal 2 — Alex persona configuration | Completed | 01:53 | 8.9% |
| Goal 3 — Manual action extension | Completed | 12:21 | 58.3% |
| Goal 4 — Final demonstration | Completed | 02:12 | 10.4% |
| **Total** | **All Goals completed** | **21:11** | **100%** |

### Initial performance interpretation

- P2 completed all four Goals within the 30-minute development-task limit.
- Persona configuration was the shortest task, requiring 1 minute and 53 seconds.
- The manual-action extension required 12 minutes and 21 seconds and accounted for approximately 58% of the total task time.
- The result suggests that basic persona authoring was efficient for this SDK-experienced participant, while code-based behavioural extension remained the main source of development effort.

Whether the tasks were completed independently, after hints, or with direct researcher assistance still needs to be confirmed and recorded.

---

## 6. P2 SUS results

### Raw responses

| SUS item | Response (1–5) | SUS contribution |
|---|---:|---:|
| 1. I think that I would like to use this SDK frequently. | 4 | 3 |
| 2. I found the SDK unnecessarily complex. | 4 | 1 |
| 3. I thought the SDK was easy to use. | 4 | 3 |
| 4. I think that I would need technical support to use this SDK. | 3 | 2 |
| 5. I found the functions in the SDK to be well integrated. | 3 | 2 |
| 6. I thought there was too much inconsistency in the SDK. | 2 | 3 |
| 7. I imagine that most Unity developers would learn to use this SDK quickly. | 4 | 3 |
| 8. I found the SDK cumbersome to use. | 2 | 3 |
| 9. I felt confident using the SDK. | 3 | 2 |
| 10. I needed to learn many things before I could get going with the SDK. | 3 | 2 |
| **Contribution total** |  | **24** |

**Calculated SUS score:** `24 × 2.5 = 60/100`

### Interpretation

P2's SUS score of 60 indicates a mixed or moderate usability judgement. This score will be treated descriptively and interpreted alongside the task-performance and interview evidence. It should not be used alone to classify the SDK's overall usability.

Item 2 requires clarification. A response of 4 indicates agreement that the SDK was unnecessarily complex, while P2 also rated the SDK as easy to use, not cumbersome, and relatively quick to learn. This may reflect a genuinely mixed judgement — easy operation despite underlying complexity — or misunderstanding of the negatively worded item. The recorded score must not be changed unless the participant explicitly confirms that the original response was entered incorrectly.

---

## 7. P2 post-task interview results

| Topic | Cleaned response | Initial interpretation |
|---|---|---|
| Easiest part | Configuring the name and other persona information | Persona fields were straightforward to understand |
| Most difficult part | Writing the code | Behavioural extension created the greatest development burden |
| Agent, Avatar, and Persona configuration | Easy to understand | Positive configuration clarity |
| Helpfulness of samples, documentation, and source code | Very helpful | Reference materials were important to task completion |
| Understanding and recovering from errors | Errors were understandable and messages were clear | Positive perceived error recoverability |
| Manual action task | Manageable | Difficult relative to other tasks, but still achievable |
| Confidence in building a real stand-in prototype | 5/7 | Moderately high confidence |
| Most valuable aspect | Reduced repetitive preliminary configuration and helped avoid omissions | SDK provided workflow and setup value beyond individual features |
| Main area for improvement | Gemini connection was sometimes slow or unstable | Cloud connection was a practical limitation |
| Future use or recommendation | Would use it again for related experiments | Positive future-use intention |

### Candidate translated quotation

> "It reduces repetitive preliminary configuration work and helps avoid omissions." — P2, translated from Chinese

The participant's original Chinese response should be retained in the raw-data record. Any quotation used in the dissertation should be marked as translated and lightly edited only for clarity.

---

## 8. Preliminary P2 findings

### 8.1 Persona configuration was efficient

P2 identified persona configuration as the easiest task, consistent with Goal 2 being completed in only 2 minutes and 10 seconds. This suggests that the SDK provides an accessible workflow for defining the basic identity and role of a virtual stand-in, at least for an external participant with previous SDK experience.

### 8.2 Behavioural extension remained the main development cost

Although P2 successfully completed the manual-action extension, Goal 3 accounted for approximately 59% of the total task time and was identified as the most difficult task. This indicates a clear transition in effort between Inspector-based configuration and code-based extension through the public API.

### 8.3 Samples and documentation supported completion

P2 described the SDK's samples, documentation, and source code as very helpful. This suggests that the toolkit's examples form an important part of its practical development workflow. The final analysis should record exactly which resources each participant used and whether completion depended on copying, adapting, or understanding the provided examples.

### 8.4 Error messages may support recovery

P2 reported that errors were understandable and that the messages were clear. This is positive evidence for debugging support, but it should be strengthened by recording the exact error, the recovery steps, and whether assistance was required.

### 8.5 Cloud connection remains a practical boundary

P2 identified the Gemini connection as the main area requiring improvement. This aligns with the broader practical concern that a toolkit may provide accessible authoring features while still depending on external cloud-service performance. The final analysis should distinguish connection setup problems, manual reconnect requirements, response latency, and general network instability.

---

## 9. Participant P3 profile and observed task process

**Anonymous identifier:** P3  
**Experience condition:** No previous IVA SDK or virtual-human project experience  
**Interpretive role:** Represents an SDK-new external-user case. P3's Unity and C# experience still needs to be recorded because the background questions were deferred during the session.

P3 reached the final working demonstration, but the completion was assisted. The transcript records researcher prompts during avatar assignment, connection recovery, persona configuration, action-API discovery, script adaptation, and component attachment. This must not be reported as independent completion.

### Task-performance results

| Goal | Completion | Time | Proportion of total task time |
|---|---|---:|---:|
| Goal 1 — Agent setup and voice interaction | Completed with assistance | 05:55 | 22.0% |
| Goal 2 — Alex persona configuration | Completed with guidance | 02:10 | 8.0% |
| Goal 3 — Manual action extension | Completed with assistance | 15:50 | 58.8% |
| Goal 4 — Final demonstration | Completed | 03:00 | 11.1% |
| **Total** | **All Goals completed** | **26:55** | **100%** |

Goal 3 was the longest stage, accounting for approximately 59% of P3's total task time. Because researcher assistance occurred during several stages, these times represent assisted task completion rather than unaided first-use performance.

### Session conditions and assistance

| Stage | Observed evidence | Coding for analysis |
|---|---|---|
| Goal 1 — Avatar and connection | P3 inspected the Agent and documentation, located the Rocketbox assets, assigned the avatar, and entered Play mode. The researcher clarified the target, directed attention to relevant Inspector fields and the setup control, and prompted reconnection. | Completed with procedural hints |
| Voice verification | Because the SDK was running on the researcher's remote computer, P3's microphone was unavailable to the application. The researcher spoke the test utterance on P3's behalf. | Function verified, but not independently by P3; remote-test deviation |
| Goal 2 — Persona | P3 configured Alex through the Inspector. The researcher pointed to fields, suggested an age, and directed copying of supplied persona text. | Completed with guidance; configuration itself was perceived as easy |
| Goal 3 — Manual action | P3 used the AgentAction documentation, identified `PerformAction`, selected an action, adapted the provided user script, compiled it, and attached it to the Agent. The researcher gave several directional hints and confirmed the relevant code area. | Assisted completion; strongest evidence of API-discoverability and documentation-dependence problems |
| Goal 4 — Demonstration | The configured agent and manual action were demonstrated successfully. | Completed |

### Observed practical issues

- The remote setup prevented direct microphone input and required researcher mediation.
- Reconnection or loading intervention was required during the initial voice test.
- P3 relied heavily on the AgentAction documentation to discover the action API and action names.
- The researcher provided multiple hints, so completion time cannot be interpreted as unaided first-use performance.
- P3 did not use the official sample or source code during the recorded process; the documentation was the main reference.

---

## 10. P3 SUS results

### Raw responses

| SUS item | Response (1–5) | SUS contribution |
|---|---:|---:|
| 1. I think that I would like to use this SDK frequently. | 4 | 3 |
| 2. I found the SDK unnecessarily complex. | 5 | 0 |
| 3. I thought the SDK was easy to use. | 3 | 2 |
| 4. I think that I would need technical support to use this SDK. | 2 | 3 |
| 5. I found the functions in the SDK to be well integrated. | 2 | 1 |
| 6. I thought there was too much inconsistency in the SDK. | 3 | 2 |
| 7. I imagine that most Unity developers would learn to use this SDK quickly. | 5 | 4 |
| 8. I found the SDK cumbersome to use. | 2 | 3 |
| 9. I felt confident using the SDK. | 3 | 2 |
| 10. I needed to learn many things before I could get going with the SDK. | 1 | 4 |
| **Contribution total** |  | **24** |

**Calculated SUS score:** `24 × 2.5 = 60/100`

P3's SUS score is the same as P2's score, but this does not mean their experiences were identical. P3 simultaneously strongly agreed that the SDK was unnecessarily complex, reported low integration, and believed Unity developers could learn it quickly. These item-level tensions should be interpreted alongside the transcript rather than reduced to the total score. No statistical or population-level interpretation will be made from the SUS results.

---

## 11. P3 post-task interview results

| Topic | Cleaned response | Initial interpretation |
|---|---|---|
| Previous relevant experience | No previous IVA SDK or virtual-human project experience | SDK-new case; Unity/C# background still missing |
| Easiest part | Configuring the name and persona fields because they were clearly visible in the Inspector | Inspector-based persona authoring was accessible |
| Most difficult part | Programming the action and locating the necessary information in the documentation | Code-based extension and API discovery were the main barriers |
| Agent, Avatar, and Persona configuration | Persona was understandable, but avatar-related fields and labels may be unclear to someone without virtual-human experience | Configuration clarity differed by component |
| Documentation, samples, and source code | Documentation was important and sometimes essential; samples and source code were not used | Strong documentation dependence |
| Understanding and recovering from errors | P3 felt able to understand where problems occurred and find solutions | Positive self-reported recoverability, qualified by researcher assistance |
| Manual action task | Conceptually easy to understand, but inefficient and more difficult to complete because it required detailed documentation search | Low conceptual difficulty but high execution effort |
| Confidence in a real stand-in prototype | Approximately 65/100 | Moderate confidence; must be reconfirmed on the requested 1–7 scale rather than silently converted |
| Concern about a real stand-in | A single free-text description may not reliably communicate detailed information in specialised scenarios | Persona authoring lacks perceived structure and precision |
| Most valuable aspect | Simple initial configuration and a low cold-start cost | The SDK lowers setup effort for basic prototypes |
| Main area for improvement | Balance simplicity with more detailed and fine-grained persona configuration | Current authoring favours simplicity over control granularity |
| Future use or recommendation | Would use it for simple tasks where the stand-in can be configured once and operate without the person being present | Positive but conditional future-use intention |

### Candidate translated quotations

> "The concept is relatively easy to understand, but completing it is less efficient because you have to search the documentation in detail." — P3, translated from Chinese

> "The current description configuration is very basic. It prioritises making configuration simple, but ignores many details." — P3, translated from Chinese

The original Chinese recording and transcript should be retained as the raw record. Quotations used in the dissertation should be checked against the audio and marked as translated.

---

## 12. Preliminary P3 findings

### 12.1 Simple configuration lowered the entry barrier

P3 considered persona fields easy to find and valued the SDK's low cold-start effort. This supports a bounded claim that the scaffolded SDK can make basic stand-in configuration approachable to an SDK-new user.

### 12.2 Avatar terminology was less self-explanatory

P3 distinguished the clear persona fields from avatar options such as character type, controller type, and associated animation settings. The transcript suggests that developers without virtual-human experience may need clearer labels, validation, presets, or contextual guidance.

### 12.3 Behavioural extension depended on documentation and assistance

The action task was understandable in principle but difficult and inefficient to execute. P3 needed to locate the relevant API, identify a compatible action name, adapt code, and attach the component, with several researcher prompts. This is evidence of an API-discoverability and workflow-support boundary rather than evidence that the feature is absent.

### 12.4 Persona simplicity created a control concern

P3 questioned whether a single description field could represent detailed information reliably in specialised stand-in scenarios. This is directly relevant to the doppelgänger use case: rapid authoring is valuable, but limited authoring structure may constrain precision, traceability, and researcher control.

### 12.5 The overall judgement was conditionally positive

P3 would use the SDK for simple tasks and believed it could reduce the need for a person to attend repeatedly after configuration. However, this willingness was conditional on task simplicity and coexisted with concerns about unnecessary complexity, feature integration, persona granularity, and action-authoring efficiency.

---

## 13. Three-case comparison table

This table will be completed after P1's self-pilot data have been integrated or reported separately.

| Measure | P1 — Researcher baseline | P2 — SDK-experienced external | P3 — SDK-new external |
|---|---:|---:|---:|
| Goal 1 time | To add from self-pilot | 04:45 | 05:55 |
| Goal 2 time | To add from self-pilot | 01:53 | 02:10 |
| Goal 3 time | To add from self-pilot | 12:21 | 15:50 |
| Goal 4 time | To add from self-pilot | 02:12 | 03:00 |
| Total task time | To add from self-pilot | 21:11 | 26:55 |
| Goals completed independently | Researcher baseline; record separately | To confirm | No; assisted completion |
| Assistance | Not applicable/self-directed | To confirm | Multiple procedural and directional hints |
| Practical deviations/errors | To add | To confirm | Remote microphone unavailable; researcher-mediated voice test; reconnect/load intervention |
| Main resource used | To add | To confirm | Official AgentAction documentation |
| SUS score | To add if collected | 60 | 60 |
| Prototype confidence | To add if collected | 5/7 | Approximately 65/100; reconfirm on 1–7 scale |
| Easiest component | To add | Persona configuration | Persona/name configuration |
| Most difficult component | To add | Code-based action extension | Code-based action extension and documentation search |
| Main perceived value | To add | Reduced setup repetition and omissions | Low cold-start effort for simple prototypes |
| Main limitation | To add | Gemini connection | Limited persona granularity and action discoverability |

### Planned comparison questions

Across the three cases, the analysis will ask:

1. Did all three experience conditions complete the same functional prototype?
2. How did total and per-Goal completion times differ across experience levels?
3. Which participants required hints or direct assistance, and at which stage?
4. Was code-based extension the main difficulty for all three experience levels?
5. Did SDK experience reduce dependence on documentation or samples?
6. Did participants encounter the same connection, configuration, or debugging problems?
7. How did SUS, confidence, and future-use intention vary across the three profiles?
8. Which findings appeared across all participants, and which were specific to one experience condition?

Differences will be described as observed patterns across these three cases, not as statistically established effects of developer experience.

---

## 14. How the study will appear in the dissertation

### Methodology

The Methodology chapter should describe:

- the rationale for selecting three contrasting experience profiles;
- participant inclusion requirements;
- the standardised scaffolded `RQ4_Starter` environment;
- the four common development Goals;
- the 30-minute development limit and think-aloud procedure;
- the standardised resource access and assistance protocol;
- collection of task time, completion, errors, resources, SUS, and interview data;
- the descriptive cross-condition analysis strategy.

### Results

The Results chapter should contain:

1. a case/profile table that distinguishes the researcher baseline from the external participants;
2. a three-case task-time and completion table;
3. assistance, errors, and resource-use results;
4. individual SUS scores plus median and range, if appropriate;
5. cross-participant qualitative themes supported by translated quotations;
6. similarities and differences across the three experience conditions.

The Results section should report the evidence without making the final suitability judgement prematurely.

### Discussion

The Discussion should interpret the comparative findings around:

- accessibility of persona and avatar configuration;
- the transition from configuration to code-based extension;
- dependence on samples, documentation, and existing Unity knowledge;
- debugging and error-recovery support;
- cloud connection and runtime limitations;
- which types of developer can realistically use the SDK and under what conditions.

### Contribution to the Main RQ

RQ1 and RQ4 will be synthesised as follows:

> RQ1 establishes whether relevant features exist and identifies their technical boundaries, while RQ4 examines whether developers with different experience levels can use a standardised subset of those features to produce a functioning virtual stand-in prototype. Their combination supports a conditional judgement of suitability based on both capability coverage and practical development effort.

The final claim should be bounded to the evaluated prototype and participant profiles. The study does not validate every possible doppelgänger experiment or establish universal SDK usability.

---

## 15. Methodological limitations to report

- The comparison contains one researcher/self-pilot baseline and only two independent external participants.
- Only one person represents each experience condition.
- The study supports structured descriptive comparison but not statistical inference.
- Prior SDK experience, Unity experience, and general programming ability may overlap and cannot be isolated with this sample.
- Remote participation, network quality, time-zone constraints, or hardware differences may influence connection and timing results.
- P3's remote microphone could not be passed through to the SDK, so the researcher performed the voice-input check on the participant's behalf.
- Assistance was not negligible in P3's session; task completion and time must therefore be interpreted together with the recorded assistance.
- Participants use a scaffolded scene, so the study evaluates configuration and extension rather than SDK installation from a completely blank project.
- Only one minimal doppelgänger/stand-in scenario is evaluated.
- SUS and interview responses are self-reported and should be triangulated with observed behaviour.

These limitations constrain the breadth of the conclusion but do not invalidate the study's exploratory comparison or its ability to identify practical developer-experience patterns.

---

## 16. Outstanding clarifications

### P2

Before final analysis, confirm the following with P2:

1. Were all Goals completed independently, or did the researcher provide hints or direct help?
2. Which sample scene, documentation page, or source file was used for each Goal?
3. What exact errors occurred, and how were they resolved?
4. Did “Gemini connection lag” refer to initial connection, manual reconnect, response latency, or network instability?
5. Was the response of 4 to SUS item 2 intentional?
6. What was the extent and frequency of P2's previous IVA SDK use?

The original recorded data should remain unchanged. Clarifications should be stored as follow-up context rather than silently replacing the raw record.

### P3

Before final analysis, confirm the following with P3 or from the session record:

1. Record P3's Unity experience, C# confidence, and any previous XR experience; the background questions were skipped during the recorded opening.
2. Ask P3 to express prototype confidence on the original 1–7 scale; retain the recorded `65/100` response in the raw data.
3. Confirm whether the SUS item 2 response of 5 was intentional.
4. Identify the exact action selected and whether the final manual gesture executed successfully.
5. Record each researcher hint using the agreed assistance coding scheme.
6. Clarify the reconnect/loading issue without attributing it to the SDK if the cause cannot be established.

The remote microphone problem is a protocol deviation and must remain visible in the Methodology or Limitations section.

---

## 17. Current preliminary conclusion

P2 and P3 provide two external-user cases with contrasting SDK experience. Both cases indicate that persona authoring can be completed relatively easily and that the SDK reduces repetitive initial configuration. Both also identify code-based behavioural extension as a more demanding part of the workflow. P2 emphasised Gemini connection performance, while P3 exposed documentation dependence, unclear avatar terminology, action discoverability problems, and a trade-off between simple persona authoring and fine-grained stand-in control.

P3's completion required substantial assistance and a researcher-mediated voice check, so the result supports a bounded claim about achievable use with documentation and support, not unaided first-use success. The conclusion remains provisional until the missing timing, experience-profile, assistance, and confidence data are completed and P1's baseline is either confirmed as procedurally comparable or reported separately as formative pilot evidence.
